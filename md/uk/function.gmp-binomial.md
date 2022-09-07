---
navigation:
  - function.gmp-and.md: « gmpand
  - function.gmp-clrbit.md: gmpclrbit »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpbinomial
---
# gmpbinomial

(PHP 7> = 7.3.0, PHP 8)

gmpbinomial - обчислює біноміальний коефіцієнт

### Опис

```methodsynopsis
gmp_binomial(GMP|int|string $n, int $k): GMP
```

Обчислює біноміальний коефіцієнт C(n, k).

### Список параметрів

`n`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`k`

### Значення, що повертаються

Повертає біноміальний коефіцієнт C(n, k).

### Помилки

Викидає [ValueError](class.valueerror.md), якщо `k` від'ємний. До PHP 8.0.0 видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція більше не повертає **`false`** у разі виникнення помилки. |
