---
navigation:
  - recursiveiteratoriterator.getmaxdepth.md: '« RecursiveIteratorIterator::getMaxDepth'
  - recursiveiteratoriterator.key.md: 'RecursiveIteratorIterator::key »'
  - index.md: PHP Manual
  - class.recursiveiteratoriterator.md: RecursiveIteratorIterator
title: 'RecursiveIteratorIterator::getSubIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveIteratorIterator::getSubIterator

(PHP 5, PHP 7, PHP 8)

RecursiveIteratorIterator::getSubIterator — Отримання активного вкладеного ітератора

### Опис

```methodsynopsis
public RecursiveIteratorIterator::getSubIterator(?int $level = null): ?RecursiveIterator
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`level`

### Значення, що повертаються

Активний вкладений ітератор у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `level` тепер допускає значення null. |
