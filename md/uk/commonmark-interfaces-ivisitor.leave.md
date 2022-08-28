Відвідування

-   [« CommonMark\\Interfaces\\IVisitor::enter](commonmark-interfaces-ivisitor.enter.html)
    
-   [CommonMark\\Interfaces\\IVisitable »](class.commonmark-interfaces-ivisitable.html)
    
-   [PHP Manual](index.html)
    
-   [CommonMark\\Interfaces\\IVisitor](class.commonmark-interfaces-ivisitor.html)
    
-   Відвідування
    

# CommonMarkInterfacesIVisitor::leave

(cmark >= 1.0.0)

CommonMarkInterfacesIVisitor::leave — Відвідування

### Опис

```methodsynopsis
abstract public CommonMark\Interfaces\IVisitor::leave(IVisitable $visitable): int|IVisitable|null
```

### Список параметрів

`visitable`

Поточний покиданий [CommonMark\\Interfaces\\IVisitable](class.commonmark-interfaces-ivisitable.html)

### Значення, що повертаються

Повернення CommonMarkInterfacesIVisitor::Done призведе до виходу допоміжного ітератора.

Повернення CommonMarkInterfacesIVisitor::Enter скине допоміжний ітератор при вході в поточний **IVisitable**

Повернення CommonMarkInterfacesIVisitor::Leave скине допоміжний ітератор при виході з поточного **IVisitable**

Повернення **IVisitable** скине допоміжний ітератор при виході з цього **IVisitable**

Якщо нічого не повертається, допоміжний ітератор продовжить роботу.

### Дивіться також

-   [CommonMark\\Interfaces\\IVisitable::accept](commonmark-interfaces-ivisitable.accept.html)