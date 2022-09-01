---
navigation:
  - function.mqseries-close.html: « mqseriesclose
  - function.mqseries-conn.html: mqseriesconn »
  - index.md: PHP Manual
  - ref.mqseries.md: Функции mqseries
title: mqseriescmit
---
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
> [mqseriesback()](function.mqseries-back.md) не працює, якщо для з'єднання з менеджером черг використовується MQSeries Client.

### Дивіться також

-   [mqseriesbegin()](function.mqseries-begin.md) - MQseries MQBEGIN
-   [mqseriesback()](function.mqseries-back.md) - MQSeries MQBACK
-   [mqseriesconn()](function.mqseries-conn.md) - MQSeries MQCONN
-   [mqseriesconnx()](function.mqseries-connx.md) - MQSeries MQCONNX
