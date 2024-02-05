---
navigation:
  - commonmark-node.accept.md: '« CommonMark\\Node::accept'
  - commonmark-interfaces-ivisitor.enter.md: 'CommonMark\\Interfaces\\IVisitor::enter »'
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Інтерфейс CommonMark\\Interfaces\\IVisitor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс CommonMark\\Interfaces\\IVisitor

(cmark >= 1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      final
      class CommonMark\Interfaces\IVisitor
     
     {
    
    /* Константы */
    
     const
     int
      Done;

    const
     int
      Enter;

    const
     int
      Leave;


    /* Методы */
    
   abstract public enter(IVisitable $visitable): int|IVisitable|null
abstract public leave(IVisitable $visitable): int|IVisitable|null

   }
```

## Зміст

-   [CommonMark\\Interfaces\\IVisitor::enter](commonmark-interfaces-ivisitor.enter.md) \- Відвідування
-   [CommonMark\\Interfaces\\IVisitor::leave](commonmark-interfaces-ivisitor.leave.md) \- Відвідування
