---
navigation:
  - class.commonmark-node-htmlinline.md: « CommonMark\\Node\\HTMLInline
  - commonmark-node-image.construct.md: 'CommonMark\\Node\\Image::\_\_construct »'
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Image успадковує CommonMark\\Node
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Image успадковує CommonMark\\Node

(cmark >= 1.0.0)

## Огляд класів

```classsynopsis



    
     
      final
      class CommonMark\Node\Image
     

     
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
      $url;

    public
     ?string
      $title;


    /* Конструктор */
    
   public __construct()
public __construct(string $url)
public __construct(string $url, string $title)


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

-   [CommonMark\\Node\\Image::\_\_construct](commonmark-node-image.construct.md) \- Конструктор класу Image
