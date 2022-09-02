---
navigation:
  - function.xmlrpc-get-type.md: « xmlrpcgettype
  - function.xmlrpc-parse-method-descriptions.md: xmlrpcparsemethoddescriptions »
  - index.md: PHP Manual
  - ref.xmlrpc.md: Функції XML-RPC
title: xmlrpcісfault
---
# xmlrpcісfault

(PHP 4> = 4.3.0, PHP 5, PHP 7)

xmlrpcісfault — Визначає, чи є масив значень уявленням помилки XMLRPC

### Опис

```methodsynopsis
xmlrpc_is_fault(array $arg): bool
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`arg`

Масив, що повертається [xmlrpcdecode()](function.xmlrpc-decode.md)

### Значення, що повертаються

Повертає **`true`**, якщо аргумент означає помилку, інакше - **`false`**. Опис помилки доступний у `$arg["faultString"]`код помилки в `$arg["faultCode"]`

### Приклади

Дивіться приклад [xmlrpcencoderequest()](function.xmlrpc-encode-request.md)

### Дивіться також

-   [xmlrpcdecode()](function.xmlrpc-decode.md) - Декодує XML у нативні типи PHP
