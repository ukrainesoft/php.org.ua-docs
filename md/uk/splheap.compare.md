---
navigation:
  - class.splheap.html: « SplHeap
  - splheap.count.html: 'SplHeap::count »'
  - index.html: PHP Manual
  - class.splheap.html: SplHeap
title: 'SplHeap::compare'
---
# SplHeap::compare

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplHeap::compare — Порівнює елементи, щоб під час сортування коректно розмістити їх у купі

### Опис

```methodsynopsis
protected SplHeap::compare(mixed $value1, mixed $value2): int
```

Порівнює `value1` з `value2`

**Увага**

Викидання винятків у методі **SplHeap::compare()** може порушити цілісність купи та перевести їх у заблокований стан. Розблокувати купу можна методом [SplHeap::recoverFromCorruption()](splheap.recoverfromcorruption.html). Однак деякі елементи можуть бути поміщені некоректно, що порушить сортування всередині купи.

### Список параметрів

`value1`

Значення першого порівнюваного вузла.

`value2`

Значення другого порівнюваного вузла.

### Значення, що повертаються

Метод повинен повертати позитивне значення, коли `value1` більше `value2`0 якщо вони рівні, і негативне в інших випадках.

> **Зауваження**
> 
> Приміщенню до купи однакових елементів небажано, оскільки неможливо буде відстежити точне положення конкретного елемента.
