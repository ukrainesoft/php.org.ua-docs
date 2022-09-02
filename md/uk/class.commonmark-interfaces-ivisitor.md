---
navigation:
  - commonmark-node.accept.md: '« CommonMarkNode::accept'
  - commonmark-interfaces-ivisitor.enter.md: 'CommonMarkInterfacesIVisitor::enter »'
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Інтерфейс CommonMarkInterfacesIVisitor
---
# Інтерфейс CommonMarkInterfacesIVisitor

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

-   [CommonMarkInterfacesIVisitor::enter](commonmark-interfaces-ivisitor.enter.md) - Відвідування
-   [CommonMarkInterfacesIVisitor::leave](commonmark-interfaces-ivisitor.leave.md) - Відвідування
