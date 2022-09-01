---
navigation:
  - function.fann-get-connection-array.html: « fanngetconnectionarray
  - function.fann-get-errno.html: fanngeterrno »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
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
