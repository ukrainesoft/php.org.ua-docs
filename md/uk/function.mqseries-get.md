---
navigation:
  - function.mqseries-disc.md: « mqseries\_disc
  - function.mqseries-inq.md: mqseries\_inq »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_get

(PECL mqseries >= 0.10.0)

mqseries\_get — MQSeries MQGET

### Опис

```methodsynopsis
mqseries_get(    resource $hConn,    resource $hObj,    array &$md,    array &$gmo,    int &$bufferLength,    string &$msg,    int &$data_length,    resource &$compCode,    resource &$reason): void
```

The**mqseries\_get()**(MQGET) call retrieves a message from a local queue that has been opened using the[mqseries\_open()](function.mqseries-open.md)(MQOPEN) call

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`hObj`

Оброблювач об'єкта.

Представляє об'єкт, що використовується.

`md`

Дескриптор повідомлення (MQMD).

`gmo`

Параметри отримання повідомлення (MQGMO).

`bufferLength`

Очікуваний розмір буфера результату

`msg`

Буфер, до якого буде поміщено вилучене повідомлення.

`data_length`

Актуальний розмір буфера

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** mqseries\_get()\*\*\*\*

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

// Устанавливаем пустой дескриптор сообщения.
    $mdg = array();
// Устанавливаем опции извлечения сообщения
    $gmo = array('Options' => MQSERIES_MQGMO_FAIL_IF_QUIESCING | MQSERIES_MQGMO_WAIT, 'WaitInterval' => 3000);

// Получаем сообщение
    mqseries_get($conn, $obj, $mdg, $gmo, 255, $msg, $data_length, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("GET CompCode:%d Reason:%d Text:%s<br>", $comp_code, $reason, mqseries_strerror($reason));
    }

// закрываем $obj
    mqseries_close($conn, $obj, MQSERIES_MQCO_NONE, $comp_code, $reason);

// закрываем соединение с менеджером
    mqseries_disc($conn, $comp_code, $reason);

?>
```

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.md) \- MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.md) \- MQSeries MQCONNX
-   [mqseries\_open()](function.mqseries-open.md) \- MQSeries MQOPEN
-   [mqseries\_put()](function.mqseries-put.md) \- MQSeries MQPUT
