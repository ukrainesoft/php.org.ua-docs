BulletList успадковує CommonMarkNode

-   [« CommonMarkNodeBlockQuote](class.commonmark-node-blockquote.html)
    
-   [CommonMarkNodeBulletList::construct »](commonmark-node-bulletlist.construct.html)
    
-   [PHP Manual](index.html)
    
-   [CommonMark](book.cmark.html)
    
-   BulletList успадковує CommonMarkNode
    

# BulletList успадковує CommonMarkNode

(cmark >= 1.0.0)

## Огляд класів

```classsynopsis


    
    
     
      final
      class CommonMark\Node\BulletList
     

     
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
     bool
      $tight;

    public
     int
      $delimiter;


    /* Конструктор */
    
   public __construct()
public __construct(int $tight)
public __construct(int $tight, int $delimiter)


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

-   [CommonMarkNodeBulletList::construct](commonmark-node-bulletlist.construct.html) - Конструктор класу BulletList