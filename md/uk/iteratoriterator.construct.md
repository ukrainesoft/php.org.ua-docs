---
navigation:
  - class.iteratoriterator.md: « IteratorIterator
  - iteratoriterator.current.md: 'IteratorIterator::current »'
  - index.md: PHP Manual
  - class.iteratoriterator.md: IteratorIterator
title: 'IteratorIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IteratorIterator::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

IteratorIterator::\_\_construct — Створює ітератор із чогось, що є обхідним (traversable)

### Опис

public**IteratorIterator::\_\_construct** [Traversable](class.traversable.md) `$iterator`, ?string`$class` **`null`**) .

Створює ітератор із чогось, що є обхідним (traversable).

### Список параметрів

`iterator`

Обхідний (traversable) ітератор.

`class`

Ім'я класу, який використовується для внутрішнього ітератора. Дозволяє вказати інший клас ітератора для обгортання наданого ітератора. За замовчуванням використовуватиметься клас `IteratorIterator`

### Дивіться також

-   [Traversable](class.traversable.md)
