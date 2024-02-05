---
navigation:
  - function.mqseries-back.md: « mqseries\_back
  - function.mqseries-close.md: mqseries\_close »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_begin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_begin

(PECL mqseries >= 0.10.0)

mqseries\_begin — MQseries MQBEGIN

### Опис

```methodsynopsis
mqseries_begin(    resource $hconn,    array $beginOptions,    resource &$compCode,    resource &$reason): void
```

Функция**mqseries\_begin()** (MQBEGIN) відкриває транзакцію, координує роботу менеджера черг та може використовувати зовнішні ресурси менеджера.

**mqseries\_begin()** стартує транзакцію . [mqseries\_back()](function.mqseries-back.md) або [mqseries\_cmit()](function.mqseries-cmit.md) - Завершують.

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

**Пример #1 Пример использования**mqseries\_begin()\*\*\*\*

```php
<?php
    $mqbo = array();
    mqseries_begin( $conn,
                    $mqbo,
                    $comp_code,
                    $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        /* код причины 2121 - предупреждающий. Смотри документацию MQSeries.*/
        if ($reason !== 2121) {
            printf("CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        }
    }
?>
```

### Примітки

> **Зауваження** :
> 
> **mqseries\_begin()** не працює, якщо для з'єднання з менеджером черг використовується MQSeries Client.

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
-   [mqseries\_back()](function.mqseries-back.md) \- MQSeries MQBACK
-   [mqseries\_cmit()](function.mqseries-cmit.md) \- MQSeries MQCMIT
