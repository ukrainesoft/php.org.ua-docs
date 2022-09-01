---
navigation:
  - multipleiterator.getflags.md: '« MultipleIterator::getFlags'
  - multipleiterator.next.md: 'MultipleIterator::next »'
  - index.md: PHP Manual
  - class.multipleiterator.md: MultipleIterator
title: 'MultipleIterator::key'
---
# MultipleIterator::key

(PHP 5> = 5.3.0, PHP 7, PHP 8)

MultipleIterator::key — Отримує зареєстровані ітератори

### Опис

```methodsynopsis
public MultipleIterator::key(): array
```

Отримує результат виконання key() зареєстрованих ітераторів.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) всіх зареєстрованих ітераторів.

### Помилки

[RuntimeException](class.runtimeexception.md), якщо ітератор недійсний (починаючи з PHP 8.1.0) або встановлено режим **`MIT_NEED_ALL`** і, принаймні, один приєднаний ітератор недійсний.

Виклик цього методу з [foreach](control-structures.foreach.html) викличе попередження "Повернений неправильний тип" ("Illegal type returned").

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер викидається виняток [RuntimeException](class.runtimeexception.md), якщо **MultipleIterator::key()** викликається на неприпустимому ітераторі. Раніше натомість поверталося значення **`false`** |

### Дивіться також

-   [MultipleIterator::current()](multipleiterator.current.md) - Отримує зареєстровані ітератори
