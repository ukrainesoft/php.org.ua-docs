---
navigation:
  - function.fann-get-connection-array.md: « fanngetconnectionarray
  - function.fann-get-errno.md: fanngeterrno »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetconnectionrate
---
# fanngetconnectionrate

(PECL fann> = 1.0.0)

fanngetconnectionrate — Отримує швидкість з'єднання, що використовується під час створення мережі

### Опис

```methodsynopsis
fann_get_connection_rate(resource $ann): float
```

Отримує швидкість з'єднання, що використовується під час створення мережі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Швидкість з'єднання, використана при створенні мережі або **`false`** у разі виникнення помилки.
