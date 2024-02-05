---
navigation:
  - function.xmlrpc-server-register-method.md: « xmlrpc\_server\_register\_method
  - refs.utilspec.windows.md: Модулі лише для Windows »
  - index.md: PHP Manual
  - ref.xmlrpc.md: Функції XML-RPC
title: xmlrpc\_set\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xmlrpc\_set\_type

(PHP 4 >= 4.1.0, PHP 5, PHP 7)

xmlrpc\_set\_type — Встановлює тип XML-RPC, base64 або datetime для значення рядка PHP

### Опис

```methodsynopsis
xmlrpc_set_type(string &$value, string $type): bool
```

Встановлює тип XML-RPC, base64 або datetime для значення рядка PHP.

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`value`

Значення для встановлення типу.

`type`

'base64' або 'datetime'

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. У разі успішного виконання, `value` конвертується в об'єкт.

### Помилки

Видає повідомлення E\_WARNING для типів XMLRPC, що не підтримуються.

### Приклади

**Приклад #1 Приклад використання** xmlrpc\_set\_type()\*\*\*\*

```php
<?php

$params = date("Ymd\TH:i:s", time());
xmlrpc_set_type($params, 'datetime');
echo xmlrpc_encode($params);

?>
```

Висновок наведеного прикладу буде схожим на:

```
<?xml version="1.0" encoding="utf-8"?>
<params>
<param>
 <value>
  <dateTime.iso8601>20090322T23:43:03</dateTime.iso8601>
 </value>
</param>
</params>
```
