Відвідування

-   [« CommonMarkInterfacesIVisitor](class.commonmark-interfaces-ivisitor.html)
    
-   [CommonMarkInterfacesIVisitor::leave »](commonmark-interfaces-ivisitor.leave.html)
    
-   [PHP Manual](index.md)
    
-   [CommonMarkInterfacesIVisitor](class.commonmark-interfaces-ivisitor.html)
    
-   Відвідування
    

# CommonMarkInterfacesIVisitor::enter

(cmark >= 1.0.0)

CommonMarkInterfacesIVisitor::enter — Відвідування

### Опис

```methodsynopsis
abstract public CommonMark\Interfaces\IVisitor::enter(IVisitable $visitable): int|IVisitable|null
```

### Список параметрів

`visitable`

Поточний вхідний [CommonMarkInterfacesIVisitable](class.commonmark-interfaces-ivisitable.html)

### Значення, що повертаються

Повернення CommonMarkInterfacesIVisitor::Done призведе до виходу допоміжного ітератора.

Повернення CommonMarkInterfacesIVisitor::Enter скине допоміжний ітератор при вході в поточний **IVisitable**

Повернення CommonMarkInterfacesIVisitor::Leave скине допоміжний ітератор при виході з поточного **IVisitable**

Повернення **IVisitable** скине допоміжний ітератор при вході до цього **IVisitable**

Якщо нічого не повертається, допоміжний ітератор продовжить роботу.

### Дивіться також

-   [CommonMarkInterfacesIVisitable::accept](commonmark-interfaces-ivisitable.accept.html)