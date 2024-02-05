---
navigation:
  - function.mqseries-cmit.md: « mqseries\_cmit
  - function.mqseries-connx.md: mqseries\_connx »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_conn
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_conn

(PECL mqseries >= 0.10.0)

mqseries\_conn — MQSeries MQCONN

### Опис

```methodsynopsis
mqseries_conn(    string $qManagerName,    resource &$hconn,    resource &$compCode,    resource &$reason): void
```

Функция**mqseries\_conn()** (MQCONN) відкриває з'єднання з менеджером черг. Вона повертає обробник з'єднання, який використовується всіма іншими функціями модуля.

### Список параметрів

`qManagerName`

Ім'я менеджера черг.

Ім'я менеджера черг, з яким встановлюється з'єднання.

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

**Пример #1 Пример использования**mqseries\_conn()\*\*\*\*

```php
<?php
    mqseries_conn('WMQ1', $conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("conn CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

### Дивіться також

-   [mqseries\_disc()](function.mqseries-disc.md) \- MQSeries MQDISC
