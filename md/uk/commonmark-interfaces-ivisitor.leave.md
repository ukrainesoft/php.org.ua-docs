---
navigation:
  - commonmark-interfaces-ivisitor.enter.md: '« CommonMark\\Interfaces\\IVisitor::enter'
  - class.commonmark-interfaces-ivisitable.md: CommonMark\\Interfaces\\IVisitable »
  - index.md: PHP Manual
  - class.commonmark-interfaces-ivisitor.md: CommonMark\\Interfaces\\IVisitor
title: 'CommonMark\\Interfaces\\IVisitor::leave'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CommonMark\\Interfaces\\IVisitor::leave

(cmark >= 1.0.0)

CommonMark\\Interfaces\\IVisitor::leave — Відвідування

### Опис

```methodsynopsis
abstract public CommonMark\Interfaces\IVisitor::leave(IVisitable $visitable): int|IVisitable|null
```

### Список параметрів

`visitable`

Поточний покиданий [CommonMark\\Interfaces\\IVisitable](class.commonmark-interfaces-ivisitable.md)

### Значення, що повертаються

Повернення CommonMark\\Interfaces\\IVisitor::Done призведе до виходу допоміжного ітератора.

Повернення CommonMark\\Interfaces\\IVisitor::Enter скине допоміжний ітератор при вході в поточний **IVisitable**

Повернення CommonMark\\Interfaces\\IVisitor::Leave скине допоміжний ітератор при виході з поточного **IVisitable**

Возврат**IVisitable** скине допоміжний ітератор при виході з цього **IVisitable**

Якщо нічого не повертається, допоміжний ітератор продовжить роботу.

### Дивіться також

-   [CommonMark\\Interfaces\\IVisitable::accept](commonmark-interfaces-ivisitable.accept.md)
