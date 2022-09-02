---
navigation:
  - function.mqseries-connx.md: « mqseriesconnx
  - function.mqseries-get.md: mqseriesget »
  - index.md: PHP Manual
  - ref.mqseries.md: Функции mqseries
title: mqseriesdisc
---
# mqseriesdisc

(PECL mqseries >= 0.10.0)

mqseriesdisc — MQSeries MQDISC

### Опис

```methodsynopsis
mqseries_disc(resource $hconn, resource &$compCode, resource &$reason): void
```

Функція **mqseriesdisc()** (MQDISC) розриває з'єднання з менеджером черг. Вона є протилежною функцій [mqseriesconn()](function.mqseries-conn.md) (MQCONN) та [mqseriesconnx()](function.mqseries-connx.md) (MQCONNX).

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

**Приклад #1 Приклад використання **mqseriesdisc()****

```php
<?php
    mqseries_disc($conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("disc CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Дивіться також

-   [mqseriesconn()](function.mqseries-conn.md) - MQSeries MQCONN
-   [mqseriesconnx()](function.mqseries-connx.md) - MQSeries MQCONNX
