MQSeries MQOPEN

-   [« mqseriesinq](function.mqseries-inq.html)
    
-   [mqseriesput1 »](function.mqseries-put1.html)
    
-   [PHP Manual](index.html)
    
-   [Функции mqseries](ref.mqseries.html)
    
-   MQSeries MQOPEN
    

# mqseriesopen

(PECL mqseries >= 0.10.0)

mqseriesopen — MQSeries MQOPEN

### Опис

```methodsynopsis
mqseries_open(    resource $hconn,    array &$objDesc,    int $option,    resource &$hobj,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesopen()** (MQOPEN) встановлює з'єднання з об'єктом.

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

**Приклад #1 Приклад використання **mqseriesopen()****

```php
<?php
    $mqods = array('ObjectName' => 'TESTQ');
    mqseries_open(
                $conn,
                $mqods,
                MQSERIES_MQOO_INPUT_AS_Q_DEF | MQSERIES_MQOO_FAIL_IF_QUIESCING | MQSERIES_MQOO_OUTPUT,
                $obj,
                $comp_code,
                $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("open CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

### Дивіться також

-   [mqseriesclose()](function.mqseries-close.html) - MQSeries MQCLOSE