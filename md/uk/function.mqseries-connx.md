---
navigation:
  - function.mqseries-conn.md: « mqseriesconn
  - function.mqseries-disc.md: mqseriesdisc »
  - index.md: PHP Manual
  - ref.mqseries.md: Функции mqseries
title: mqseriesconnx
---
# mqseriesconnx

(PECL mqseries >= 0.10.0)

mqseriesconnx — MQSeries MQCONNX

### Опис

```methodsynopsis
mqseries_connx(    string $qManagerName,    array &$connOptions,    resource &$hconn,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesconnx()** (MQCONNX) відкриває з'єднання з менеджером черг. Вона повертає обробник з'єднання, який використовується всіма іншими функціями модуля.

Виклик функції **mqseriesconnx()** аналогічний виклику [mqseriesconn()](function.mqseries-conn.md) (MQCONN), за винятком того, що MQCONNX дозволяє встановити опції, що визначають режим роботи з менеджером.

### Список параметрів

`qManagerName`

Ім'я менеджера черг.

Ім'я менеджера черг, з яким встановлюється з'єднання.

`connOps`

Опції, що визначають роботу функцій

Дивіться структуру MQCNO.

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

**Приклад #1 Приклад використання **mqseriesconnx()****

```php
<?php
    $mqcno = array(
        'Version' => MQSERIES_MQCNO_VERSION_2,
        'Options' => MQSERIES_MQCNO_STANDARD_BINDING,
        'MQCD' => array('ChannelName' => 'MQNX9420.CLIENT',
        'ConnectionName' => 'localhost',
        'TransportType' => MQSERIES_MQXPT_TCP)
    );

    mqseries_connx('MQNX9420', $mqcno, $conn, $comp_code,$reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("Connx CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }

?>
```

**Приклад #2 Приклад використання **mqseriesconnx()** з використанням SSL та URL відповідача OCSP**

```php
<?php
    $mqcno = array(
        'Version' => 4, //MQCNO_VERSION_4
        'Options' => MQSERIES_MQCNO_STANDARD_BINDING,
        'MQCD' => array(
            'Version' => 7, //MQCD_VERSION_7
            'ConnectionName' => 'localhost',
            'TransportType' => MQSERIES_MQXPT_TCP,
            'ChannelName' => 'CONNECTIONCHANNEL',
            'SSLCipherSpec' => 'NULL_SHA'
        ),
        'MQSCO' => array(
            'KeyRepository' => '/var/mqm/qmgrs/QUEUEMGR/ssl/key', //Local path where the SSL key repository can be found
            'MQAIR' => array(
                'Version' => 2, //MQAIR_VERSION_2
                'AuthInfoType' => 2, //MQAIT_OCSP
                'OCSPResponderURL' => 'http://dummy.OCSP.responder'
            )
        )
    );

    mqseries_connx('QUEUEMGR', $mqcno, $conn, $comp_code,$reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("Connx CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }

?>
```

### Дивіться також

-   [mqseriesdisc()](function.mqseries-disc.md) - MQSeries MQDISC
