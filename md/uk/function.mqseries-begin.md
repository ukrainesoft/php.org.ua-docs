MQseries MQBEGIN

-   [« mqseries\_back](function.mqseries-back.html)
    
-   [mqseries\_close »](function.mqseries-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции mqseries](ref.mqseries.html)
    
-   MQseries MQBEGIN
    

# mqseriesbegin

(PECL mqseries >= 0.10.0)

mqseriesbegin — MQseries MQBEGIN

### Опис

```methodsynopsis
mqseries_begin(    resource $hconn,    array $beginOptions,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesbegin()** (MQBEGIN) відкриває транзакцію, координує роботу менеджера черг та може використовувати зовнішні ресурси менеджера.

**mqseriesbegin()** стартує транзакцію . [mqseries\_back()](function.mqseries-back.html) або [mqseries\_cmit()](function.mqseries-cmit.html) - Завершують.

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

-   [mqseries\_conn()](function.mqseries-conn.html) - MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.html) - MQSeries MQCONNX
-   [mqseries\_back()](function.mqseries-back.html) - MQSeries MQBACK
-   [mqseries\_cmit()](function.mqseries-cmit.html) - MQSeries MQCMIT