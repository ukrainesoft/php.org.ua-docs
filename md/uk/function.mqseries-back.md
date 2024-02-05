---
navigation:
  - ref.mqseries.md: « Функції mqseries
  - function.mqseries-begin.md: mqseries\_begin »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_back
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_back

(PECL mqseries >= 0.10.0)

mqseries\_back — MQSeries MQBACK

### Опис

```methodsynopsis
mqseries_back(resource $hconn, resource &$compCode, resource &$reason): void
```

Функция**mqseries\_back()** (MQBACK) здійснює відкат транзакції. Тобто. всі повідомлення, розміщені в чергу з останньої точки синхронізації, видаляються з неї. Всі повідомлення, прочитані з черги з останньої точки синхронізації, відновлюються (стають доступними).

Using**mqseries\_back()** працює тільки спільно з [mqseries\_begin()](function.mqseries-begin.md) і тільки якщо використовується пряме з'єднання з менеджером черг, а не через інтерфейс mqclient.

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

**Пример #1 Пример использования**mqseries\_back()\*\*\*\*

```php
<?php
    mqseries_back($conn, $comp_code, $reason);

    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Примітки

> **Зауваження** :
> 
> **mqseries\_back()** не працює, якщо для з'єднання з менеджером черг використовується MQSeries Client.

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
-   [mqseries\_begin()](function.mqseries-begin.md) \- MQseries MQBEGIN
