---
navigation:
  - function.mqseries-back.html: « mqseriesback
  - function.mqseries-close.html: mqseriesclose »
  - index.md: PHP Manual
  - ref.mqseries.md: Функции mqseries
title: mqseriesbegin
---
# mqseriesbegin

(PECL mqseries >= 0.10.0)

mqseriesbegin — MQseries MQBEGIN

### Опис

```methodsynopsis
mqseries_begin(    resource $hconn,    array $beginOptions,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesbegin()** (MQBEGIN) відкриває транзакцію, координує роботу менеджера черг та може використовувати зовнішні ресурси менеджера.

**mqseriesbegin()** стартує транзакцію . [mqseriesback()](function.mqseries-back.html) або [mqseriescmit()](function.mqseries-cmit.html) - Завершують.

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

**Приклад #1 Приклад використання **mqseriesbegin()****

```php
<?php
    $mqbo = array();
    mqseries_begin( $conn,
                    $mqbo,
                    $comp_code,
                    $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        /* код причины 2121 - предупреждающий. Смотри документацию MQSeries.*/
        if ($reason !== 2121) {
            printf("CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        }
    }
?>
```

### Примітки

> **Зауваження**
> 
> **mqseriesbegin()** не працює, якщо для з'єднання з менеджером черг використовується MQSeries Client.

### Дивіться також

-   [mqseriesconn()](function.mqseries-conn.html) - MQSeries MQCONN
-   [mqseriesconnx()](function.mqseries-connx.html) - MQSeries MQCONNX
-   [mqseriesback()](function.mqseries-back.html) - MQSeries MQBACK
-   [mqseriescmit()](function.mqseries-cmit.html) - MQSeries MQCMIT
