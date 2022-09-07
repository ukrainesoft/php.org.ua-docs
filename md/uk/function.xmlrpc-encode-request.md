---
navigation:
  - function.xmlrpc-decode.md: « xmlrpcdecode
  - function.xmlrpc-encode.md: xmlrpcencode »
  - index.md: PHP Manual
  - ref.xmlrpc.md: Функції XML-RPC
title: xmlrpcencoderequest
---
# xmlrpcencoderequest

(PHP 4> = 4.1.0, PHP 5, PHP 7)

xmlrpcencoderequest — генерує XML для методу запиту

### Опис

```methodsynopsis
xmlrpc_encode_request(string $method, mixed $params, array $output_options = ?): string
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`method`

Ім'я методу виклику.

`params`

Параметри методу, сумісні із сигнатурою виклику.

`output_options`

Масив, що уточнює параметри виведення, може містити (значення за замовчуванням виділено):

-   outputtype: php, *xml*
    
-   verbosity: nowhitespace, newlinesonly, *pretty*
    
-   escaping: cdata, *non-ascii, non-print, markup* (може бути рядок з одним значенням або масив з кількома значеннями)
    
-   version: simple, *xmlrpc*, soap 1.1, auto
    
-   encoding: *iso-8859-1*, інший набір символів, що підтримується iconv
    

### Значення, що повертаються

Повертає рядок, що містить запит на запит XML.

### Приклади

**Приклад #1 Приклад клієнтської функції XMLRPC**

```php
<?php
$request = xmlrpc_encode_request("method", array(1, 2, 3));
$context = stream_context_create(array('http' => array(
    'method' => "POST",
    'header' => "Content-Type: text/xml",
    'content' => $request
)));
$file = file_get_contents("http://www.example.com/xmlrpc", false, $context);
$response = xmlrpc_decode($file);
if ($response && xmlrpc_is_fault($response)) {
    trigger_error("xmlrpc: $response[faultString] ($response[faultCode])");
} else {
    print_r($response);
}
?>
```

### Дивіться також

-   [streamcontextcreate()](function.stream-context-create.md) - Створює контекст потоку
-   [filegetcontents()](function.file-get-contents.md) - Читає вміст файлу в рядок
-   [xmlrpcdecode()](function.xmlrpc-decode.md) - Декодує XML у нативні типи PHP
