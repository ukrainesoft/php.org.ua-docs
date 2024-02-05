---
navigation:
  - function.gmp-and.md: « gmp\_and
  - function.gmp-clrbit.md: gmp\_clrbit »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_binomial
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_binomial

(PHP 7 >= 7.3.0, PHP 8)

gmp\_binomial - обчислює біноміальний коефіцієнт

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

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не повертає \*\*`false`\*\*в случае возникновения ошибки. |
