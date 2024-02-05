---
navigation:
  - function.mqseries-inq.md: « mqseries\_inq
  - function.mqseries-put1.md: mqseries\_put1 »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_open

(PECL mqseries >= 0.10.0)

mqseries\_open — MQSeries MQOPEN

### Опис

```methodsynopsis
mqseries_open(    resource $hconn,    array &$objDesc,    int $option,    resource &$hobj,    resource &$compCode,    resource &$reason): void
```

Функция**mqseries\_open()** (MQOPEN) встановлює з'єднання з об'єктом.

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`objDesc`

Дескриптор об'єкт. (MQOD)

`options`

Опції, що визначають роботу функцій

`hObj`

Оброблювач об'єкта.

Представляє об'єкт, що використовується.

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** mqseries\_open()\*\*\*\*

```php
<?php
    $mqods = array('ObjectName' => 'TESTQ');
    mqseries_open(
                $conn,
                $mqods,
                MQSERIES_MQOO_INPUT_AS_Q_DEF | MQSERIES_MQOO_FAIL_IF_QUIESCING | MQSERIES_MQOO_OUTPUT,
                $obj,
                $comp_code,
                $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("open CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

### Дивіться також

-   [mqseries\_close()](function.mqseries-close.md) \- MQSeries MQCLOSE
