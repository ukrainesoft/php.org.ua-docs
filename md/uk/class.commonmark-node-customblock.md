---
navigation:
  - commonmark-node-link.construct.md: '« CommonMark\\Node\\Link::\_\_construct'
  - class.commonmark-node-custominline.md: CommonMark\\Node\\CustomInline »
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: CustomBlock успадковує CommonMark\\Node
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CustomBlock успадковує CommonMark\\Node

(cmark >= 1.0.0)

## Огляд класів

```classsynopsis



    
     
      final
      class CommonMark\Node\CustomBlock
     

     
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
     ?string
      $onEnter;

    public
     ?string
      $onLeave;


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
