---
navigation:
  - class.splmaxheap.md: « SplMaxHeap
  - class.splminheap.md: SplMinHeap »
  - index.md: PHP Manual
  - class.splmaxheap.md: SplMaxHeap
title: 'SplMaxHeap::compare'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplMaxHeap::compare

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplMaxHeap::compare — Порівнює елементи, щоб під час сортування коректно розмістити їх у купі

### Опис

```methodsynopsis
protected SplMaxHeap::compare(mixed $value1, mixed $value2): int
```

Сравнивает`value1`с`value2`

### Список параметрів

`value1`

Значення першого порівнюваного вузла.

`value2`

Значення другого порівнюваного вузла.

### Значення, що повертаються

Метод повертає позитивне значення, коли `value1`больше`value2`0 якщо вони рівні, і негативне в інших випадках.

> **Зауваження** :
> 
> Наявність кількох елементів з однаковим значенням купі не рекомендується, оскільки неможливо буде відстежити точне положення конкретного елемента.
