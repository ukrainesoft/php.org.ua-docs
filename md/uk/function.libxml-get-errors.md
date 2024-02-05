---
navigation:
  - function.libxml-disable-entity-loader.md: « libxml\_disable\_entity\_loader
  - function.libxml-get-external-entity-loader.md: libxml\_get\_external\_entity\_loader »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxml\_get\_errors
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# libxml\_get\_errors

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

libxml\_get\_errors — Отримання масиву помилок, що відбулися.

### Опис

```methodsynopsis
libxml_get_errors(): array
```

Отримання масиву помилок, що відбулися.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив об'єктів [LibXMLError](class.libxmlerror.md)якщо в буфері є помилки, або порожній масив в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** libxml\_get\_errors()\*\*\*\*

Цей приклад демонструє, як створити простий обробник помилок libxml.

```php
<?php

libxml_use_internal_errors(true);

$xmlstr = <<< XML
<?xml version='1.0' standalone='yes'?>
<movies>
 <movie>
  <titles>PHP: Behind the Parser</title>
 </movie>
</movies>
XML;

$doc = simplexml_load_string($xmlstr);
$xml = explode("\n", $xmlstr);

if ($doc === false) {
    $errors = libxml_get_errors();

    foreach ($errors as $error) {
        echo display_xml_error($error, $xml);
    }

    libxml_clear_errors();
}


function display_xml_error($error, $xml)
{
    $return  = $xml[$error->line - 1] . "\n";
    $return .= str_repeat('-', $error->column) . "^\n";

    switch ($error->level) {
        case LIBXML_ERR_WARNING:
            $return .= "Warning $error->code: ";
            break;
         case LIBXML_ERR_ERROR:
            $return .= "Error $error->code: ";
            break;
        case LIBXML_ERR_FATAL:
            $return .= "Fatal Error $error->code: ";
            break;
    }

    $return .= trim($error->message) .
               "\n  Line: $error->line" .
               "\n  Column: $error->column";

    if ($error->file) {
        $return .= "\n  File: $error->file";
    }

    return "$return\n\n--------------------------------------------\n\n";
}

?>
```

Результат виконання наведеного прикладу:

```
<titles>PHP: Behind the Parser</title>
----------------------------------------------^
Fatal Error 76: Opening and ending tag mismatch: titles line 4 and title
  Line: 4
  Column: 46

--------------------------------------------
```

### Дивіться також

-   [libxml\_get\_last\_error()](function.libxml-get-last-error.md) \- Вилучення останньої помилки з libxml
-   [libxml\_clear\_errors()](function.libxml-clear-errors.md) \- Очищення буфера помилок libxml
