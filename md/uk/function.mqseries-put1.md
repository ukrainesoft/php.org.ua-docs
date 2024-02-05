---
navigation:
  - function.mqseries-open.md: « mqseries\_open
  - function.mqseries-put.md: mqseries\_put »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_put1
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_put1

(PECL mqseries >= 0.10.0)

mqseries\_put1 — MQSeries MQPUT1

### Опис

```methodsynopsis
mqseries_put1(    resource $hconn,    resource &$objDesc,    resource &$msgDesc,    resource &$pmo,    string $buffer,    resource &$compCode,    resource &$reason): void
```

Функция**mqseries\_put1()** (MQPUT1) містить повідомлення в чергу. Черга має бути не відкрита.

Для надсилання повідомлення в чергу ви можете використовувати як [mqseries\_put()](function.mqseries-put.md), так и**mqseries\_put1()**. . [mqseries\_put()](function.mqseries-put.md) (MQPUT) використовується коли необхідно помістити в чергу кілька повідомлень, у той час як **mqseries\_put1()** (MQPUT1) зручно використовувати для одного повідомлення. По суті, ця функція включає послідовність викликів MQOPEN, MQPUT і MQCLOSE, що дозволяє не викликати окремо.

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`objDesc`

Object descriptor. (MQOD)

Дескриптор об'єкта (черги), куди необхідно помістити повідомлення.

`msgDesc`

Дескриптор повідомлення (MQMD).

`pmo`

Опції повідомлення, що додається (MQPMO).

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
-   [mqseries\_open()](function.mqseries-open.md) \- MQSeries MQOPEN
-   [mqseries\_get()](function.mqseries-get.md) \- MQSeries MQGET
