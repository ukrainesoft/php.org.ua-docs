---
navigation:
  - function.fann-reset-errstr.md: « fannreseterrstr
  - function.fann-run.md: fannrun »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannresetMSE
---
# fannresetMSE

(PECL fann> = 1.0.0)

fannresetMSE — Скидає середньоквадратичну помилку з мережі

### Опис

```methodsynopsis
fann_reset_MSE(string $ann): bool
```

Скидає середньоквадратичну помилку з мережі.

Функція також скидає кількість бітів, що вийшли з ладу.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetMSE()](function.fann-get-mse.md) - Зчитує середньоквадратичну помилку мережі
-   [fanngetbitfail()](function.fann-get-bit-fail.md) - Кількість бітів збою
-   [fanngetbitfaillimit()](function.fann-get-bit-fail-limit.md) - Повертає межу збою бітів, використану під час навчання
