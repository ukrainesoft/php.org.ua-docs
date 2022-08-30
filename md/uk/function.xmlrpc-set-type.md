Встановлює тип XML-RPC, base64 або datetime для значення рядка PHP

-   [« xmlrpcserverregistermethod](function.xmlrpc-server-register-method.html)
    
-   [Модулі лише для Windows »](refs.utilspec.windows.html)
    
-   [PHP Manual](index.html)
    
-   [Функції XML-RPC](ref.xmlrpc.html)
    
-   Встановлює тип XML-RPC, base64 або datetime для значення рядка PHP
    

# xmlrpcsettype

(PHP 4> = 4.1.0, PHP 5, PHP 7)

xmlrpcsettype — Встановлює тип XML-RPC, base64 або datetime для значення рядка PHP

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

Видає повідомлення EWARNING для типів XMLRPC, що не підтримуються.

### Приклади

**Приклад #1 Приклад використання **xmlrpcsettype()****

```php
<?php

$params = date("Ymd\TH:i:s", time());
xmlrpc_set_type($params, 'datetime');
echo xmlrpc_encode($params);

?>
```

Результатом виконання цього прикладу буде щось подібне:

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