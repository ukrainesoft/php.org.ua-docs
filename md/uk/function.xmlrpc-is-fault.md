---
navigation:
  - function.xmlrpc-get-type.md: « xmlrpc\_get\_type
  - function.xmlrpc-parse-method-descriptions.md: xmlrpc\_parse\_method\_descriptions »
  - index.md: PHP Manual
  - ref.xmlrpc.md: Функції XML-RPC
title: xmlrpc\_is\_fault
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xmlrpc\_is\_fault

(PHP 4 >= 4.3.0, PHP 5, PHP 7)

xmlrpc\_is\_fault — Визначає, чи є масив значень уявленням помилки XMLRPC

### Опис

```methodsynopsis
xmlrpc_is_fault(array $arg): bool
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`arg`

Масив, що повертається [xmlrpc\_decode()](function.xmlrpc-decode.md)

### Значення, що повертаються

Повертає **`true`**, якщо аргумент означає помилку, інакше - \*\*`false`\*\*Опис ошибки доступно в`$arg["faultString"]`,а код ошибки в`$arg["faultCode"]`

### Приклади

Смотрите пример[xmlrpc\_encode\_request()](function.xmlrpc-encode-request.md)

### Дивіться також

-   [xmlrpc\_decode()](function.xmlrpc-decode.md) \- Декодує XML у нативні типи PHP
