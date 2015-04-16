---
layout: post
title:  "XPath Extension Types: Web Scraping"
date:   2015-04-16 16:15:00pm
description: Three new XPath structures for use in web scraping.
categories:
- data mining
- scraping
- web data extraction
permalink: xpath-scraping
---

Note: this post is an appendix reference for a paper, "Social Data Extraction through Canopied Feature Hashing with Nested Structure Detection".

XPath Extension Types
---------------------

XPath [^clark_xml_1999] is a language designed to locate and extract elements within structural XML documents, including HTML. It can select the attributes or values of single or multiple tags at any depth within the XML tree, using direct paths or searching by predicates. XPath is a commonly-used scraping tool, and are often used in data extraction wrappers due to their simplicity. This section introduces a couple of extended uses for XPath that are particularly useful for data extraction.

### Structural XPaths

A structural XPath can locate elements in a DOM tree based on a minimal set of available elements. This provides the ability to find objects within the DOM tree that match certain tag layouts, which is useful for tree-matching algorithms. An example of a structural XPath is shown in Fig. 1, which also illustrates that the structural XPath can be generated to different tree depths.

~~~perl
// li [ count(a)=1 and count(h3)=1 and count(p)=3 ]
// li [ count(a)=1 and count(h3)=1 and count(p)=3 and p [ count(span)=2 ] ]
~~~
Figure 1. Two example structural XPaths: to depth [1, 2]

An algorithm to generate a structural XPath is presented in Listing \ref{lst:sde:structure_xpath}. At each level of the tree, the tag types of children are counted. By using the XPath predicate `count()`, elements that contain a precise number of certain tag types can be selected. By going deeper into the tree, more complex structures can be selected because only elements that exactly match the predicate in each branch of the tree will satisfy the search. Leniency is allowed for structures that contain tags not mentioned by the predicates, as only tags mentioned in a `count()` predicate are checked.

~~~python
function RecursiveStructureXPath(tag, depth, level=0)
    if tag.children and level != depth then
        child_count = count of tag.children by tag type
        path_parts = list("count(child.type)=child.count" for child in sorted(child_count))
        recursed_children = list(RecursiveStructureXPath(child, depth, level+1) for child in tag.children)
        children_xpath = join(path_parts, " and ")
        
        if children_xpath then
            children_xpath = "[ children_xpath ]"
            
    if children_xpath then
        return "tag.name children_xpath

function StructureXPath(tag, depth)
    return "//" + RecursiveStructureXPath(tag, depth)
~~~
Listing 1. Generating a Structural XPath to a specific depth

Once generated, a structural XPath can be given to an XPath engine and used to locate elements that match the structure described. For data extraction, these XPaths are used to locate elements that match the generated wrapper, and fields can then be derived from those elements using relative XPaths, described in the following section.

### Relative XPath

Relative XPath can be used to navigate from one element to another, if elements are ancestrally related. This provides a simple way of expressing particular fields within a parent element, which is useful for data extraction. A couple of examples of relative XPaths are shown in Fig. 2.

~~~perl
ul[1]/li[1]/h3[1]
li[1]/a[1]
span[2]/p[4]/li[2]
~~~
Figure 2. Three example relative xpaths, navigating from one point in the tree to another

An algorithm to generate a relative XPath is presented in Listing 2. Starting at the child, the sibling position of the tag is determined before walking up the tree. Once the parent is reached, the XPath is developed. In order to support a broader range of returned data than standard XPath, the retrieval engine is extended to include several more options, such as `inner_text` and `string`.

~~~python
function RelativeXPath(tag, target)
    path_components = list()
    loop
        if tag == target then
            break
        else
            if tag.parent then
                path_components += SiblingPosition(tag)
                tag = tag.parent
            else
                path_components += tag.name
                break
    xpath = join(path_components, "/")
    return xpath
~~~
Listing 2. Generating a relative XPath from one tag to a parent

### Identifying XPath

An identifying XPath can be used to locate a specific element in the DOM tree, even if the element is not otherwise unique. While some wrappers use tag position to select elements, this is not always reliable - selecting the 15th element in a list won't work on a data structure that only has 13 elements. To work around this, we instead attempt to locate the nearest unique ancestor and derive a relative XPath from that element. A couple of examples are shown in Fig. 3.

~~~perl
//ul[@id="comments"]/li[3]
//ul[contains(@class, "comments-paginate") and contains(@class, "page")]/li[2]
~~~

Figure 3. Two example identifying XPaths, from one point to its nearest unique parent

Similar to relative XPaths, the creation of an identifying XPath starts at the child and walks up the tree until a unique parent is discovered. This can be an element with an ID attribute (which are unique) or a set of classes that are likely to be unique - or at least fairly discerning. In some cases, this may be the element itself - in which case, the identifying XPath is quite simple. In others, we must walk several levels up to find a unique parent. An algorithm to generate identifying XPaths is presented in Listing 3.

~~~python
function IdentifyingXPath(tag, target)
    path_components = list()
    loop
        if tag == target then
            break
        else
            if tag.id then
                path = "tag.name[@id='tag.id']"
                path_components += path
                break
            else if tag.classes then
                class_paths = list("contains(@class, 'cls')" for cls in tag.classes)
                path = "tag.name[join(class_paths, ' and ']"
                break
            else
                if tag.parent then
                    path_components += SiblingPosition(tag)
                    tag = tag.parent
                else
                    path_components += tag.name
                    break
    xpath = join(path_components, "/")
    return xpath
~~~
Listing 3. Generating an identifying XPath from one tag to a parent

Identifying XPaths are particularly useful for finding and locating specific elements, rather than similar structures. They can be used to express and locate buttons, links or pagination elements.

[^clark_xml_1999]: Clark, J., & DeRose, S. (1999). XML path language (XPath) version 1.0. Retrieved from http://www.faa.gov/nextgen/programs/swim/documentation/media/compliancy/Xpathv1.0.pdf
