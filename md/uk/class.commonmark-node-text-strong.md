Strong успадковує CommonMarkNode

-   [« CommonMarkNodeText::construct](commonmark-node-text.construct.html)
    
-   [CommonMarkNodeTextEmphasis »](class.commonmark-node-text-emphasis.html)
    
-   [PHP Manual](index.html)
    
-   [CommonMark](book.cmark.html)
    
-   Strong успадковує CommonMarkNode
    

# Strong успадковує CommonMarkNode

(cmark >= 1.0.0)

## Огляд класів

```classsynopsis


    
    
     
      final
      class CommonMark\Node\Text\Strong
     

     
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