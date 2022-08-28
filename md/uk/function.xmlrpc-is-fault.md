Визначає, чи є масив значень уявленням помилки XMLRPC

-   [« xmlrpc\_get\_type](function.xmlrpc-get-type.html)
    
-   [xmlrpc\_parse\_method\_descriptions »](function.xmlrpc-parse-method-descriptions.html)
    
-   [PHP Manual](index.html)
    
-   [Функции XML-RPC](ref.xmlrpc.html)
    
-   Визначає, чи є масив значень уявленням помилки XMLRPC
    

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

Масив, що повертається [xmlrpc\_decode()](function.xmlrpc-decode.html)

### Значення, що повертаються

Повертає **`true`**, якщо аргумент означає помилку, інакше - **`false`**. Опис помилки доступний у `$arg["faultString"]`код помилки в `$arg["faultCode"]`

### Приклади

Дивіться приклад [xmlrpc\_encode\_request()](function.xmlrpc-encode-request.html)

### Дивіться також

-   [xmlrpc\_decode()](function.xmlrpc-decode.html) - Декодує XML у нативні типи PHP