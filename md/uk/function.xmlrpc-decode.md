---
navigation:
  - function.xmlrpc-decode-request.html: « xmlrpcdecoderequest
  - function.xmlrpc-encode-request.html: xmlrpcencoderequest »
  - index.md: PHP Manual
  - ref.xmlrpc.md: Функції XML-RPC
title: xmlrpcdecode
---
# xmlrpcdecode

(PHP 4> = 4.1.0, PHP 5, PHP 7)

xmlrpcdecode — Декодує XML у типові типи PHP

### Опис

```methodsynopsis
xmlrpc_decode(string $xml, string $encoding = "iso-8859-1"): mixed
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`xml`

XML-відповідь, що повертається методом XMLRPC.

`encoding`

Вхідне кодування, яке підтримується iconv.

### Значення, що повертаються

Повертає масив, чи число, чи рядок, чи логічне значення відповідно до відповіді, що повертається методом XMLRPC.

### Приклади

Дивіться приклад [xmlrpcencoderequest()](function.xmlrpc-encode-request.md)

### Дивіться також

-   [xmlrpcencoderequest()](function.xmlrpc-encode-request.md) - Генерує XML для методу запиту
-   [xmlrpcісfault()](function.xmlrpc-is-fault.md) - Визначає, чи є масив значень уявленням помилки XMLRPC
