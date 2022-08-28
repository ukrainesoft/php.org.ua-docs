MQSeries MQINQ

-   [« mqseries\_get](function.mqseries-get.html)
    
-   [mqseries\_open »](function.mqseries-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции mqseries](ref.mqseries.html)
    
-   MQSeries MQINQ
    

# mqseriesinq

(PECL mqseries >= 0.10.0)

mqseriesinq — MQSeries MQINQ

### Опис

```methodsynopsis
mqseries_inq(    resource $hconn,    resource $hobj,    int $selectorCount,    array $selectors,    int $intAttrCount,    resource &$intAttr,    int $charAttrLength,    resource &$charAttr,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesinq()** (MQINQ) повертає масив цілих чисел та набір рядків, що містять атрибути об'єкта.

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`hObj`

Оброблювач об'єкта.

Представляє об'єкт, що використовується.

`selectorCount`

Кількість селекторів.

`selectors`

Масив селекторів атрибутів.

`intAttrLength`

Кількість цілих атрибутів.

`intAttr`

Масив цілісних атрибутів.

`charAttrLength`

Довжина буфера символьні атрибути.

`charAttr`

Символьні атрибути.

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **mqseriesinq()****

```php
<?php
    $int_attr = array();
    $char_attr = "";

    mqseries_inq($conn, $obj, 1, array(MQSERIES_MQCA_Q_MGR_NAME), 0, $int_attr, 48, $char_attr, $comp_code, $reason);

    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("INQ CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    } else {
        echo "INQ QManager name result ".$char_attr."<br>\n";
    }
?>
```

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.html) - MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.html) - MQSeries MQCONNX
-   [mqseries\_open()](function.mqseries-open.html) - MQSeries MQOPEN