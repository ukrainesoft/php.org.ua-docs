---
navigation:
  - function.mqseries-cmit.html: « mqseriescmit
  - function.mqseries-connx.html: mqseriesconnx »
  - index.md: PHP Manual
  - ref.mqseries.md: Функции mqseries
title: mqseriesconn
---
# mqseriesconn

(PECL mqseries >= 0.10.0)

mqseriesconn - MQSeries MQCONN

### Опис

```methodsynopsis
mqseries_conn(    string $qManagerName,    resource &$hconn,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesconn()** (MQCONN) відкриває з'єднання з менеджером черг. Вона повертає обробник з'єднання, який використовується всіма іншими функціями модуля.

### Список параметрів

`qManagerName`

Ім'я менеджера черг.

Ім'я менеджера черг, з яким встановлюється з'єднання.

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

**Приклад #1 Приклад використання **mqseriesconn()****

```php
<?php
    mqseries_conn('WMQ1', $conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("conn CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

### Дивіться також

-   [mqseriesdisc()](function.mqseries-disc.html) - MQSeries MQDISC
