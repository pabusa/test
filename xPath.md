# XPath

[XML Path Language (XPath) 3.1](https://www.w3.org/TR/2017/REC-xpath-31-20170321/)

## Introduction

https://www.freeformatter.com/xpath-tester.html

The primary purpose of XPath is to address the nodes of XML trees and JSON trees. XPath gets its name from its use of a path notation for navigating through the hierarchical structure of an XML document. XPath uses a compact, non-XML syntax to facilitate use of XPath within URIs and XML attribute values. XPath 3.1 adds a similar syntax for navigating JSON trees.

[...]
Because these languages are so closely related, their grammars and language descriptions are generated from a common source to ensure consistency, and the editors of these specifications work together closely.[...]

## Basics

The basic building block of XPath 3.1 is the **expression** [...] The language provides several kinds of expressions which may be constructed from keywords, symbols, and operands. In general, the operands of an expression are other expressions. XPath 3.1 allows expressions to be nested with full generality.

XPath 3.1 is a case-sensitive language.

[A.3 Reserved Function Names](https://www.w3.org/TR/2017/REC-xpath-31-20170321/#id-reserved-fn-names)

- A **sequence** is a ordered collection of 0 or more *items*.
- An **item** is either:
  - An *atomic* value
  - A *node* is 
  - A *function*

## Nodes
There are seven kinds of Nodes in the data model: 
1. Document
2. Element
3. Attribute
4. Text
5. Namespace
6. Processing instruction
7. Comment
   
All nodes must satisfy the following general constraints:
1. Every node must have a unique identity, distinct from all other nodes.
2. The children property of a node must not contain two consecutive Text Nodes.
3. The children property of a node must not contain any empty Text Nodes.
4. No node may appear more than once in the children or attributes properties of a node.

Each kind of node is described in the following sections.

### Document nodes
Document Nodes encapsulate XML documents. Documents have the following properties:
- base-uri, possibly empty.
- children, possibly empty.
- unparsed-entities, possibly empty.
- document-uri, possibly empty.
- string-value
- typed-value

Document Nodes must satisfy the following constraints.

1. The children must consist exclusively of Element, Processing Instruction, Comment, and Text Nodes if it is not empty. Attribute, Namespace, and Document Nodes can never appear as children
2. If a node N is among the children of a Document Node D, then the parent of N must be D.
3. If a node N has a parent Document Node D, then N must be among the children of D.
4. The string-value property of a Document Node must be the concatenation of the string-values of all its Text Node descendants in document order or, if the document has no such descendants, the zero-length string.

----------------123
### Element nodes
### Attribute nodes
### Text nodes
### Namespace nodes
### Processing instruction nodes
### Comment nodes

```
<rutaRelativa> ::= [ <eje> ] <prueba> [ <predicado> ]
```
