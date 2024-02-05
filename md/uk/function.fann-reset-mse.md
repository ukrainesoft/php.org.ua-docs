---
navigation:
  - function.fann-reset-errstr.md: « fann\_reset\_errstr
  - function.fann-run.md: fann\_run »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_reset\_MSE
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_reset\_MSE

(PECL fann >= 1.0.0)

fann\_reset\_MSE — Скидає середньоквадратичну помилку з мережі

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

-   [fann\_get\_MSE()](function.fann-get-mse.md) \- Зчитує середньоквадратичну помилку мережі
-   [fann\_get\_bit\_fail()](function.fann-get-bit-fail.md) \- Кількість бітів збою
-   [fann\_get\_bit\_fail\_limit()](function.fann-get-bit-fail-limit.md) \- Повертає межу збою бітів, використану під час навчання
