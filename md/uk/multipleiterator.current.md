---
navigation:
  - multipleiterator.countiterators.md: '« MultipleIterator::countIterators'
  - multipleiterator.detachiterator.md: 'MultipleIterator::detachIterator »'
  - index.md: PHP Manual
  - class.multipleiterator.md: MultipleIterator
title: 'MultipleIterator::current'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MultipleIterator::current

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

MultipleIterator::current — Отримує зареєстровані ітератори

### Опис

```methodsynopsis
public MultipleIterator::current(): array
```

Отримує результат виконання current() зареєстрованих ітераторів.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) всіх поточних значень кожного приєднаного ітератора.

### Помилки

[RuntimeException](class.runtimeexception.md), якщо ітератор недійсний (починаючи з PHP 8.1.0) або встановлено режим **`MIT_NEED_ALL`** і, принаймні, один приєднаний ітератор недійсний. Або **IllegalValueException**якщо ключ має значення **`null`**, а флаг\*\*`MIT_KEYS_ASSOC`\*\*установлен.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Тепер викидається виняток[RuntimeException](class.runtimeexception.md), якщо [MultipleIterator::key()](multipleiterator.key.md) викликається на неприпустимому ітераторі. Раніше натомість поверталося значення **`false`** |

### Дивіться також

-   [MultipleIterator::valid()](multipleiterator.valid.md) \- Перевіряє коректність підитераторів
