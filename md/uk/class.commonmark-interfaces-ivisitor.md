Інтерфейс CommonMarkInterfacesIVisitor

-   [« CommonMarkNode::accept](commonmark-node.accept.html)
    
-   [CommonMarkInterfacesIVisitor::enter »](commonmark-interfaces-ivisitor.enter.html)
    
-   [PHP Manual](index.html)
    
-   [CommonMark](book.cmark.html)
    
-   Інтерфейс CommonMarkInterfacesIVisitor
    

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

-   [CommonMarkInterfacesIVisitor::enter](commonmark-interfaces-ivisitor.enter.html) - Відвідування
-   [CommonMarkInterfacesIVisitor::leave](commonmark-interfaces-ivisitor.leave.html) - Відвідування