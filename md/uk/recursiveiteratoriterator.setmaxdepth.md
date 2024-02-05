---
navigation:
  - recursiveiteratoriterator.rewind.md: '« RecursiveIteratorIterator::rewind'
  - recursiveiteratoriterator.valid.md: 'RecursiveIteratorIterator::valid »'
  - index.md: PHP Manual
  - class.recursiveiteratoriterator.md: RecursiveIteratorIterator
title: 'RecursiveIteratorIterator::setMaxDepth'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveIteratorIterator::setMaxDepth

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

RecursiveIteratorIterator::setMaxDepth — Встановлення максимальної глибини вкладеності

### Опис

```methodsynopsis
public RecursiveIteratorIterator::setMaxDepth(int $maxDepth = -1): void
```

Задає максимальну глибину вкладеності елементів.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`maxDepth`

Максимально допустима глибина вкладеності . `-1` знімає обмеження на глибину рекурсії.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [Exception](class.exception.md), якщо аргумент `maxDepth`меньше`-1`
