---
navigation:
  - class.commonmark-node-linebreak.html: « CommonMarkNodeLineBreak
  - class.commonmark-node-codeblock.html: CommonMarkNodeCodeBlock »
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Code успадковує CommonMarkNode
---
# Code успадковує CommonMarkNode

(cmark >= 1.0.0)

## Огляд класів

```classsynopsis



    
     
      final
      class CommonMark\Node\Code
     

     
      extends
       CommonMark\Node\Text
     

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

    public
     ?string
      $literal;


    /* Конструктор */
    
   public CommonMark\Node\Text::__construct()
public CommonMark\Node\Text::__construct(string $literal)


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
