Отримання масиву помилок, що відбулися

-   [« libxmldisableentityloader](function.libxml-disable-entity-loader.html)
    
-   [libxmlgetlasterror »](function.libxml-get-last-error.html)
    
-   [PHP Manual](index.md)
    
-   [Функції libxml](ref.libxml.md)
    
-   Отримання масиву помилок, що відбулися
    

# libxmlgeterrors

(PHP 5> = 5.1.0, PHP 7, PHP 8)

libxmlgeterrors — Отримання масиву помилок, що відбулися.

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

**Приклад #1 Приклад використання **libxmlgeterrors()****

Цей приклад демонструє, як створити простий обробник помилок libxml.

```php
<?php

libxml_use_internal_errors(true);

$xmlstr = <<< XML
<?xml version='1.0' standalone='yes'?>
<movies>
 <movie>
  <titles>PHP: Behind the Parser</title>
 </movie>
</movies>
XML;

$doc = simplexml_load_string($xmlstr);
$xml = explode("\n", $xmlstr);

if ($doc === false) {
    $errors = libxml_get_errors();

    foreach ($errors as $error) {
        echo display_xml_error($error, $xml);
    }

    libxml_clear_errors();
}


function display_xml_error($error, $xml)
{
    $return  = $xml[$error->line - 1] . "\n";
    $return .= str_repeat('-', $error->column) . "^\n";

    switch ($error->level) {
        case LIBXML_ERR_WARNING:
            $return .= "Warning $error->code: ";
            break;
         case LIBXML_ERR_ERROR:
            $return .= "Error $error->code: ";
            break;
        case LIBXML_ERR_FATAL:
            $return .= "Fatal Error $error->code: ";
            break;
    }

    $return .= trim($error->message) .
               "\n  Line: $error->line" .
               "\n  Column: $error->column";

    if ($error->file) {
        $return .= "\n  File: $error->file";
    }

    return "$return\n\n--------------------------------------------\n\n";
}

?>
```

Результат виконання цього прикладу:

```
<titles>PHP: Behind the Parser</title>
----------------------------------------------^
Fatal Error 76: Opening and ending tag mismatch: titles line 4 and title
  Line: 4
  Column: 46

--------------------------------------------
```

### Дивіться також

-   [libxmlgetlasterror()](function.libxml-get-last-error.html) - Вилучення останньої помилки з libxml
-   [libxmlclearerrors()](function.libxml-clear-errors.html) - Очищення буфера помилок libxml