MQSeries MQPUT1

-   [« mqseries\_open](function.mqseries-open.html)
    
-   [mqseries\_put »](function.mqseries-put.html)
    
-   [PHP Manual](index.html)
    
-   [Функции mqseries](ref.mqseries.html)
    
-   MQSeries MQPUT1
    

# mqseriesput1

(PECL mqseries >= 0.10.0)

mqseriesput1 - MQSeries MQPUT1

### Опис

```methodsynopsis
mqseries_put1(    resource $hconn,    resource &$objDesc,    resource &$msgDesc,    resource &$pmo,    string $buffer,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesput1()** (MQPUT1) містить повідомлення в чергу. Черга має бути не відкрита.

Для надсилання повідомлення в чергу ви можете використовувати як [mqseries\_put()](function.mqseries-put.html), так і **mqseriesput1()**. . [mqseries\_put()](function.mqseries-put.html) (MQPUT) використовується коли необхідно помістити в чергу кілька повідомлень, у той час як **mqseriesput1()** (MQPUT1) зручно використовувати для одного повідомлення. По суті, ця функція включає послідовність викликів MQOPEN, MQPUT і MQCLOSE, що дозволяє не викликати окремо.

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`objDesc`

Object descriptor. (MQOD)

Дескриптор об'єкта (черги), куди необхідно помістити повідомлення.

`msgDesc`

Дескриптор повідомлення (MQMD).

`pmo`

Опції повідомлення, що додається (MQPMO).

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mqseries\_conn()](function.mqseries-conn.html) - MQSeries MQCONN
-   [mqseries\_connx()](function.mqseries-connx.html) - MQSeries MQCONNX
-   [mqseries\_open()](function.mqseries-open.html) - MQSeries MQOPEN
-   [mqseries\_get()](function.mqseries-get.html) - MQSeries MQGET