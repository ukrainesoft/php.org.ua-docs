---
navigation:
  - class.multipleiterator.md: « MultipleIterator
  - multipleiterator.construct.md: 'MultipleIterator::construct »'
  - index.md: PHP Manual
  - class.multipleiterator.md: MultipleIterator
title: 'MultipleIterator::attachIterator'
---
# MultipleIterator::attachIterator

(PHP 5> = 5.3.0, PHP 7, PHP 8)

MultipleIterator::attachIterator — Приєднує ітератор

### Опис

```methodsynopsis
public MultipleIterator::attachIterator(Iterator $iterator, string|int|null $info = null): void
```

Приєднує ітератор.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`iterator`

Новий ітератор для приєднання.

`info`

Асоціативна інформація для ітератора (Iterator), яка має бути представлена ​​цілим числом (int), рядком (string), або **`null`**

### Значення, що повертаються

Опис...

### Помилки

**IlegallegalValueException**, якщо параметр `iterator` недійсний, або якщо `info` містить асоційовану інформацію.

### Дивіться також

-   [MultipleIterator::construct()](multipleiterator.construct.md) - Створює новий MultipleIterator
