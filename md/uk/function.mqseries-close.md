---
navigation:
  - function.mqseries-begin.md: « mqseries\_begin
  - function.mqseries-cmit.md: mqseries\_cmit »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_close

(PECL mqseries >= 0.10.0)

mqseries\_close — MQSeries MQCLOSE

### Опис

```methodsynopsis
mqseries_close(    resource $hconn,    resource $hobj,    int $options,    resource &$compCode,    resource &$reason): void
```

Функция**mqseries\_close()** (MQCLOSE) припиняє доступ до об'єкта і є зворотною функцією [mqseries\_open()](function.mqseries-open.md)(MQOPEN).

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`hObj`

Оброблювач об'єкта.

Представляє об'єкт, що використовується.

`options`

`compCode`

Completion code.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**mqseries\_close()\*\*\*\*

```php
<?php
    mqseries_close($conn, $obj, MQSERIES_MQCO_NONE, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("close CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### Дивіться також

-   [mqseries\_open()](function.mqseries-open.md) \- MQSeries MQOPEN
-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
