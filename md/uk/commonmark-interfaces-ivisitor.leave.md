---
navigation:
  - commonmark-interfaces-ivisitor.enter.md: '« CommonMarkInterfacesIVisitor::enter'
  - class.commonmark-interfaces-ivisitable.md: CommonMarkInterfacesIVisitable »
  - index.md: PHP Manual
  - class.commonmark-interfaces-ivisitor.md: CommonMarkInterfacesIVisitor
title: 'CommonMarkInterfacesIVisitor::leave'
---
# CommonMarkInterfacesIVisitor::leave

(cmark >= 1.0.0)

CommonMarkInterfacesIVisitor::leave — Відвідування

### Опис

```methodsynopsis
abstract public CommonMark\Interfaces\IVisitor::leave(IVisitable $visitable): int|IVisitable|null
```

### Список параметрів

`visitable`

Поточний покиданий [CommonMarkInterfacesIVisitable](class.commonmark-interfaces-ivisitable.md)

### Значення, що повертаються

Повернення CommonMarkInterfacesIVisitor::Done призведе до виходу допоміжного ітератора.

Повернення CommonMarkInterfacesIVisitor::Enter скине допоміжний ітератор при вході в поточний **IVisitable**

Повернення CommonMarkInterfacesIVisitor::Leave скине допоміжний ітератор при виході з поточного **IVisitable**

Повернення **IVisitable** скине допоміжний ітератор при виході з цього **IVisitable**

Якщо нічого не повертається, допоміжний ітератор продовжить роботу.

### Дивіться також

-   [CommonMarkInterfacesIVisitable::accept](commonmark-interfaces-ivisitable.accept.md)
