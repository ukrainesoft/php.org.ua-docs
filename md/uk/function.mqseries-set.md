---
navigation:
  - function.mqseries-put.md: « mqseries\_put
  - function.mqseries-strerror.md: mqseries\_strerror »
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_set

(PECL mqseries >= 0.10.0)

mqseries\_set — MQSeries MQSET

### Опис

```methodsynopsis
mqseries_set(    resource $hConn,    resource $hObj,    int $selectorCount,    array $selectors,    int $intAttrCount,    array $intAttrs,    int $charAttrLength,    array $charAttrs,    resource &$compCode,    resource &$reason): void
```

Функция**mqseries\_set()**(MQSET) используется для изменения атрибутов очереди.

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

-   [mqseries\_inq()](function.mqseries-inq.md) \- MQSeries MQINQ
