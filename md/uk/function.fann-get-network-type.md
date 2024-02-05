---
navigation:
  - function.fann-get-mse.md: « fann\_get\_MSE
  - function.fann-get-num-input.md: fann\_get\_num\_input »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_network\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_network\_type

(PECL fann >= 1.0.0)

fann\_get\_network\_type — Отримує тип нейронної мережі

### Опис

```methodsynopsis
fann_get_network_type(resource $ann): int
```

Отримує тип нейронної мережі, де вона була створена.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа[типу мережі](fann.constants.md#constants.fann-nettype)или\*\*`false`\*\*в случае возникновения ошибки.
