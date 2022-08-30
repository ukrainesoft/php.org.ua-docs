MQSeries MQSET

-   [« mqseriesput](function.mqseries-put.html)
    
-   [mqseriesstrerror »](function.mqseries-strerror.html)
    
-   [PHP Manual](index.html)
    
-   [Функции mqseries](ref.mqseries.html)
    
-   MQSeries MQSET
    

# mqseriesset

(PECL mqseries >= 0.10.0)

mqseriesset — MQSeries MQSET

### Опис

```methodsynopsis
mqseries_set(    resource $hConn,    resource $hObj,    int $selectorCount,    array $selectors,    int $intAttrCount,    array $intAttrs,    int $charAttrLength,    array $charAttrs,    resource &$compCode,    resource &$reason): void
```

Функція **mqseriesset()** (MQSET) використовується для зміни атрибутів черги.

### Список параметрів

`hConn`

Оброблювач з'єднання.

Є відкрите з'єднання з менеджером черг.

`hObj`

Object handle.

Об'єкт, що використовується.

`selectorCount`

Кількість селекторів.

`selectors`

Масив селекторів атрибутів.

`intAttrCount`

Кількість цілих атрибутів.

`intAttrs`

Масив цілісних атрибутів.

`charAttrLength`

Розмір буфера рядкових атрибутів.

`charAttrs`

Строкові атрибути.

`compCode`

Код завершення.

`reason`

Код причини, що кваліфікує compCode.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mqseriesinq()](function.mqseries-inq.html) - MQSeries MQINQ