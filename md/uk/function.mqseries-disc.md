---
navigation:
  - function.mqseries-connx.md: « mqseries\_connx
  - function.mqseries-get.md: mqseries\_get »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_disc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_disc

(PECL mqseries >= 0.10.0)

mqseries\_disc — MQSeries MQDISC

### Опис

```methodsynopsis
mqseries_disc(resource $hconn, resource &$compCode, resource &$reason): void
```

Функция**mqseries\_disc()** (MQDISC) розриває з'єднання з менеджером черг. Вона є протилежною функцій [mqseries\_conn()](function.mqseries-conn.md)(MQCONN) и[mqseries\_connx()](function.mqseries-connx.md)(MQCONNX).

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** mqseries\_disc()\*\*\*\*

```php
<?php
    mqseries_disc($conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("disc CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
