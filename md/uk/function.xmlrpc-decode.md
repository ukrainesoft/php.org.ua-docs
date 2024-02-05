---
navigation:
  - function.xmlrpc-decode-request.md: « xmlrpc\_decode\_request
  - function.xmlrpc-encode-request.md: xmlrpc\_encode\_request »
  - index.md: PHP Manual
  - ref.xmlrpc.md: Функції XML-RPC
title: xmlrpc\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xmlrpc\_decode

(PHP 4 >= 4.1.0, PHP 5, PHP 7)

xmlrpc\_decode — Декодує XML у типові типи PHP

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

Смотрите пример[xmlrpc\_encode\_request()](function.xmlrpc-encode-request.md)

### Дивіться також

-   [xmlrpc\_encode\_request()](function.xmlrpc-encode-request.md) \- Генерує XML для методу запиту
-   [xmlrpc\_is\_fault()](function.xmlrpc-is-fault.md) \- Визначає, чи є масив значень уявленням помилки XMLRPC
