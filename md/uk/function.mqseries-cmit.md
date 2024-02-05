---
navigation:
  - function.mqseries-close.md: « mqseries\_close
  - function.mqseries-conn.md: mqseries\_conn »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_cmit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_cmit

(PECL mqseries >= 0.10.0)

mqseries\_cmit — MQSeries MQCMIT

### Опис

```methodsynopsis
mqseries_cmit(resource $hconn, resource &$compCode, resource &$reason): void
```

Функция**mqseries\_cmit()** (MQCMIT) фіксує транзакцію. Тобто. всі повідомлення, розміщені в чергу з останньої точки синхронізації, стають постійними. Усі повідомлення, прочитані з черги з останньої точки синхронізації, видаляються з неї.

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

**Пример #1 Пример использования**mqseries\_cmit()\*\*\*\*

```php
<?php
    mqseries_cmit($conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("cmit CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Примітки

> **Зауваження** :
> 
> [mqseries\_back()](function.mqseries-back.md) не працює, якщо для з'єднання з менеджером черг використовується MQSeries Client.

### Дивіться також

-   [mqseries\_begin()](function.mqseries-begin.md) \- MQseries MQBEGIN
-   [mqseries\_back()](function.mqseries-back.md) \- MQSeries MQBACK
-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
