---
navigation:
  - function.mqseries-put1.md: « mqseries\_put1
  - function.mqseries-set.md: mqseries\_set »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_put
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_put

(PECL mqseries >= 0.10.0)

mqseries\_put — MQSeries MQPUT

### Опис

```methodsynopsis
mqseries_put(    resource $hConn,    resource $hObj,    array &$md,    array &$pmo,    string $message,    resource &$compCode,    resource &$reason): void
```

Функция**mqseries\_put()** (MQPUT) містить повідомлення в чергу або список розподілу. Черга, або список розподілу, мають бути відкриті.

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`hObj`

Оброблювач об'єкта.

Представляє об'єкт, що використовується.

`md`

Дескриптор повідомлення (MQMD).

`pmo`

Опції повідомлення, що додається (MQPMO).

`message`

Саме повідомлення.

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**mqseries\_put()\*\*\*\*

```php
<?php
// Открываем соединение с MQ
    mqseries_conn('WMQ1', $conn, $comp_code, $reason);
// Теперь $conn содержит ссылку на соединение

// Открываем соединение с очередью testq
    mqseries_open(
                $conn,
                array('ObjectName' => 'TESTQ'),
                MQSERIES_MQOO_INPUT_AS_Q_DEF | MQSERIES_MQOO_FAIL_IF_QUIESCING | MQSERIES_MQOO_OUTPUT,
                $obj,
                $comp_code,
                $reason);
// Теперь $obj содержит ссылку на объект (TESTQ)

// Настраиваем массив дескриптора сообщения. Читайте руководство MQSeries.
    $md = array(
                'Version' => MQSERIES_MQMD_VERSION_1,
                'Expiry' => MQSERIES_MQEI_UNLIMITED,
                'Report' => MQSERIES_MQRO_NONE,
                'MsgType' => MQSERIES_MQMT_DATAGRAM,
                'Format' => MQSERIES_MQFMT_STRING,
                'Priority' => 1,
                'Persistence' => MQSERIES_MQPER_PERSISTENT);

// Настраиваем опции добавления сообщения.
    $pmo = array('Options' => MQSERIES_MQPMO_NEW_MSG_ID|MQSERIES_MQPMO_SYNCPOINT);

// кладём сообщение 'Ping' в очередь.
    mqseries_put($conn, $obj, $md, $pmo, 'Ping', $comp_code, $reason);

    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("put CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }

// Закрываем обработчик объекта $obj
    mqseries_close($conn, $obj, MQSERIES_MQCO_NONE, $comp_code, $reason);

// Закрываем соединение с менеджером.
    mqseries_disc($conn, $comp_code, $reason);

?>
```

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
-   [mqseries\_open()](function.mqseries-open.md) \- MQSeries MQOPEN
-   [mqseries\_get()](function.mqseries-get.md) \- MQSeries MQGET
