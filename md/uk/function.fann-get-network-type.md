---
navigation:
  - function.fann-get-mse.html: « fanngetMSE
  - function.fann-get-num-input.html: fanngetnuminput »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetnetworktype
---
# fanngetnetworktype

(PECL fann> = 1.0.0)

fanngetnetworktype — Отримує тип нейронної мережі

### Опис

```methodsynopsis
fann_get_network_type(resource $ann): int
```

Отримує тип нейронної мережі, де вона була створена.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа [типа сети](fann.constants.html#constants.fann-nettype) або **`false`** у разі виникнення помилки.
