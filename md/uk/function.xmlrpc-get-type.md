---
navigation:
  - function.xmlrpc-encode.md: « xmlrpcencode
  - function.xmlrpc-is-fault.md: xmlrpcісfault »
  - index.md: PHP Manual
  - ref.xmlrpc.md: Функції XML-RPC
title: xmlrpcgettype
---
# xmlrpcgettype

(PHP 4> = 4.1.0, PHP 5, PHP 7)

xmlrpcgettype — Отримує тип XML-RPC для значення PHP

### Опис

```methodsynopsis
xmlrpc_get_type(mixed $value): string
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

Ця функція особливо корисна для base64 та рядка, що містить дату.

### Список параметрів

`value`

Значення PHP

### Значення, що повертаються

Повертає тип XML-RPC.

### Приклади

**Приклад #1 Приклад XML-RPC типу**

```php
<?php
echo xmlrpc_get_type(null) . "\n"; // base64
echo xmlrpc_get_type(false) . "\n"; // boolean
echo xmlrpc_get_type(1) . "\n"; // int
echo xmlrpc_get_type(1.0) . "\n"; // double
echo xmlrpc_get_type("") . "\n"; // string
echo xmlrpc_get_type(array()) . "\n"; // array
echo xmlrpc_get_type(new stdClass) . "\n"; // array
echo xmlrpc_get_type(STDIN) . "\n"; // int
?>
```

### Дивіться також

-   [xmlrpcsettype()](function.xmlrpc-set-type.md) - Встановлює тип XML-RPC, base64 або datetime для значення рядка PHP
