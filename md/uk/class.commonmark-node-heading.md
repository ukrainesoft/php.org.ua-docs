---
navigation:
  - class.commonmark-node-document.md: « CommonMarkNodeDocument
  - commonmark-node-heading.construct.md: 'CommonMarkNodeHeading::construct »'
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Heading успадковує CommonMarkNode
---
# Heading успадковує CommonMarkNode

(cmark >= 1.0.0)

## Огляд класів

```classsynopsis


    
    
     
      final
      class CommonMark\Node\Heading
     

     
      extends
       CommonMark\Node
     

     implements 
       CommonMark\Interfaces\IVisitable,  Traversable {
    

    /* Наследуемые свойства */
    
     public
     readonly
     ?Node
      $parent;
public
     readonly
     ?Node
      $previous;
public
     readonly
     ?Node
      $next;
public
     readonly
     ?Node
      $lastChild;
public
     readonly
     ?Node
      $firstChild;
public
     readonly
     int
      $startLine;
public
     readonly
     int
      $endLine;
public
     readonly
     int
      $startColumn;
public
     readonly
     int
      $endColumn;


    /* Свойства */
    public
     int
      $level;


    /* Конструктор */
    
   public __construct()
public __construct(int $level)


    /* Наследуемые методы */
    public CommonMark\Node::appendChild(CommonMark\Node $child): CommonMark\Node
public CommonMark\Node::prependChild(CommonMark\Node $child): CommonMark\Node
public CommonMark\Node::insertAfter(CommonMark\Node $sibling): CommonMark\Node
public CommonMark\Node::insertBefore(CommonMark\Node $sibling): CommonMark\Node
public CommonMark\Node::replace(CommonMark\Node $target): CommonMark\Node
public CommonMark\Node::unlink(): void
public CommonMark\Node::accept(CommonMark\Interfaces\IVisitor $visitor): void


   }
```

## Зміст

-   [CommonMarkNodeHeading::construct](commonmark-node-heading.construct.md) - Конструктор класу Heading
