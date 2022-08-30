MQSeries MQCMIT

-   [« mqseriesclose](function.mqseries-close.html)
    
-   [mqseriesconn »](function.mqseries-conn.html)
    
-   [PHP Manual](index.md)
    
-   [Функции mqseries](ref.mqseries.md)
    
-   MQSeries MQCMIT
    

# mqseriescmit

(PECL mqseries >= 0.10.0)

mqseriescmit — MQSeries MQCMIT

### Опис

```methodsynopsis
mqseries_cmit(resource $hconn, resource &$compCode, resource &$reason): void
```

Функція **mqseriescmit()** (MQCMIT) фіксує транзакцію. Тобто. всі повідомлення, розміщені в чергу з останньої точки синхронізації, стають постійними. Усі повідомлення, прочитані з черги з останньої точки синхронізації, видаляються з неї.

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

**Приклад #1 Приклад використання **mqseriescmit()****

```php
<?php
    mqseries_cmit($conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("cmit CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Примітки

> **Зауваження**
> 
> [mqseriesback()](function.mqseries-back.html) не працює, якщо для з'єднання з менеджером черг використовується MQSeries Client.

### Дивіться також

-   [mqseriesbegin()](function.mqseries-begin.html) - MQseries MQBEGIN
-   [mqseriesback()](function.mqseries-back.html) - MQSeries MQBACK
-   [mqseriesconn()](function.mqseries-conn.html) - MQSeries MQCONN
-   [mqseriesconnx()](function.mqseries-connx.html) - MQSeries MQCONNX