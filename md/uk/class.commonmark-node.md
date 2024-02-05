---
navigation:
  - class.commonmark-node-custominline.md: « CommonMark\\Node\\CustomInline
  - commonmark-node.appendchild.md: 'CommonMark\\Node::appendChild »'
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Анотація класу CommonMark\\Node
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Анотація класу CommonMark\\Node

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

-   [CommonMark\\Node::appendChild](commonmark-node.appendchild.md) \- Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::prependChild](commonmark-node.prependchild.md) \- Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::insertAfter](commonmark-node.insertafter.md) \- Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::insertBefore](commonmark-node.insertbefore.md) \- Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::replace](commonmark-node.replace.md) \- Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::unlink](commonmark-node.unlink.md) \- Маніпуляції з AST (Абстрактне синтаксичне дерево)
-   [CommonMark\\Node::accept](commonmark-node.accept.md)— Visitation
