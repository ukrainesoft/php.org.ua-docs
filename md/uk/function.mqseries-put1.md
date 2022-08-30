MQSeries MQPUT1

-   [« mqseriesopen](function.mqseries-open.html)
    
-   [mqseriesput »](function.mqseries-put.html)
    
-   [PHP Manual](index.md)
    
-   [Функции mqseries](ref.mqseries.md)
    
-   MQSeries MQPUT1
    

# mqseriesput1

(PECL mqseries >= 0.10.0)

mqseriesput1 - MQSeries MQPUT1

### Опис

```methodsynopsis
mqseries_put1(    resource $hconn,    resource &$objDesc,    resource &$msgDesc,    resource &$pmo,    string $buffer,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesput1()** (MQPUT1) містить повідомлення в чергу. Черга має бути не відкрита.

Для надсилання повідомлення в чергу ви можете використовувати як [mqseriesput()](function.mqseries-put.html), так і **mqseriesput1()**. . [mqseriesput()](function.mqseries-put.html) (MQPUT) використовується коли необхідно помістити в чергу кілька повідомлень, у той час як **mqseriesput1()** (MQPUT1) зручно використовувати для одного повідомлення. По суті, ця функція включає послідовність викликів MQOPEN, MQPUT і MQCLOSE, що дозволяє не викликати окремо.

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

-   [mqseriesconn()](function.mqseries-conn.html) - MQSeries MQCONN
-   [mqseriesconnx()](function.mqseries-connx.html) - MQSeries MQCONNX
-   [mqseriesopen()](function.mqseries-open.html) - MQSeries MQOPEN
-   [mqseriesget()](function.mqseries-get.html) - MQSeries MQGET