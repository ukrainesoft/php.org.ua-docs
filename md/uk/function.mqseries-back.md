---
navigation:
  - ref.mqseries.md: « Функции mqseries
  - function.mqseries-begin.md: mqseriesbegin »
  - index.md: PHP Manual
  - ref.mqseries.md: Функции mqseries
title: mqseriesback
---
# mqseriesback

(PECL mqseries >= 0.10.0)

mqseriesback — MQSeries MQBACK

### Опис

```methodsynopsis
mqseries_back(resource $hconn, resource &$compCode, resource &$reason): void
```

Функція **mqseriesback()** (MQBACK) здійснює відкат транзакції. Тобто. всі повідомлення, розміщені в чергу з останньої точки синхронізації, видаляються з неї. Всі повідомлення, прочитані з черги з останньої точки синхронізації, відновлюються (стають доступними).

Using **mqseriesback()** працює тільки спільно з [mqseriesbegin()](function.mqseries-begin.md) і тільки якщо використовується пряме з'єднання з менеджером черг, а не через інтерфейс mqclient.

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

**Приклад #1 Приклад використання **mqseriesback()****

```php
<?php
    mqseries_back($conn, $comp_code, $reason);

    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Примітки

> **Зауваження**
> 
> **mqseriesback()** не працює, якщо для з'єднання з менеджером черг використовується MQSeries Client.

### Дивіться також

-   [mqseriesconn()](function.mqseries-conn.md) - MQSeries MQCONN
-   [mqseriesconnx()](function.mqseries-connx.md) - MQSeries MQCONNX
-   [mqseriesbegin()](function.mqseries-begin.md) - MQseries MQBEGIN
