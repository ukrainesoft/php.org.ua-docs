Анотація класу CommonMarkNode

-   [« CommonMark\\Node\\CustomInline](class.commonmark-node-custominline.html)
    
-   [CommonMark\\Node::appendChild »](commonmark-node.appendchild.html)
    
-   [PHP Manual](index.html)
    
-   [CommonMark](book.cmark.html)
    
-   Анотація класу CommonMarkNode
    

# Анотація класу CommonMarkNode

(cmark >= 1.0.0)

## Вступ

Являє абстрактний вузол, не призначений для безпосереднього використання програмістом.

## Огляд класів

```classsynopsis



    
     
      final
      abstract
      class CommonMark\Node
     

     implements 
       CommonMark\Interfaces\IVisitable,  Traversable {

    /* Свойства */
    
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


    /* Методы */
    
   public appendChild(CommonMark\Node $child): CommonMark\Node
public prependChild(CommonMark\Node $child): CommonMark\Node
public insertAfter(CommonMark\Node $sibling): CommonMark\Node
public insertBefore(CommonMark\Node $sibling): CommonMark\Node
public replace(CommonMark\Node $target): CommonMark\Node
public unlink(): void
public accept(CommonMark\Interfaces\IVisitor $visitor): void

   }
```

## Зміст

-   [CommonMark\\Node::appendChild](commonmark-node.appendchild.html) - Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::prependChild](commonmark-node.prependchild.html) - Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::insertAfter](commonmark-node.insertafter.html) - Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::insertBefore](commonmark-node.insertbefore.html) - Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::replace](commonmark-node.replace.html) - Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::unlink](commonmark-node.unlink.html) - Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::accept](commonmark-node.accept.html) - Visitation