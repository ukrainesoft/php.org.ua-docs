---
navigation:
  - function.mqseries-begin.html: « mqseriesbegin
  - function.mqseries-cmit.html: mqseriescmit »
  - index.md: PHP Manual
  - ref.mqseries.md: Функции mqseries
title: mqseriesclose
---
# mqseriesclose

(PECL mqseries >= 0.10.0)

mqseriesclose — MQSeries MQCLOSE

### Опис

```methodsynopsis
mqseries_close(    resource $hconn,    resource $hobj,    int $options,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesclose()** (MQCLOSE) припиняє доступ до об'єкта і є зворотною функцією [mqseriesopen()](function.mqseries-open.html) (MQOPEN).

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`hObj`

Оброблювач об'єкта.

Представляє об'єкт, що використовується.

`options`

`compCode`

Completion code.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **mqseriesclose()****

```php
<?php
    mqseries_close($conn, $obj, MQSERIES_MQCO_NONE, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("close CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Дивіться також

-   [mqseriesopen()](function.mqseries-open.html) - MQSeries MQOPEN
-   [mqseriesconn()](function.mqseries-conn.html) - MQSeries MQCONN
-   [mqseriesconnx()](function.mqseries-connx.html) - MQSeries MQCONNX
