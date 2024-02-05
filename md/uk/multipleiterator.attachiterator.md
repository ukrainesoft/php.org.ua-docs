---
navigation:
  - class.multipleiterator.md: « MultipleIterator
  - multipleiterator.construct.md: 'MultipleIterator::\_\_construct »'
  - index.md: PHP Manual
  - class.multipleiterator.md: MultipleIterator
title: 'MultipleIterator::attachIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MultipleIterator::attachIterator

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

MultipleIterator::attachIterator — Приєднує ітератор

### Опис

```methodsynopsis
public MultipleIterator::attachIterator(Iterator $iterator, string|int|null $info = null): void
```

Приєднує ітератор.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`iterator`

Новий ітератор для приєднання.

`info`

Асоціативна інформація для ітератора (Iterator), яка має бути представлена ​​цілим числом (int), рядком (string), або **`null`**

### Значення, що повертаються

Опис...

### Помилки

**IllegalValueException**, якщо параметр `iterator` недійсний, або якщо `info` містить асоційовану інформацію.

### Дивіться також

-   [MultipleIterator::\_\_construct()](multipleiterator.construct.md) \- Створює новий MultipleIterator
