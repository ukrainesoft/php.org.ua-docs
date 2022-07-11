- [« libxml_disable_entity_loader](function.libxml-disable-entity-loader.md)
- [libxml_get_last_error »](function.libxml-get-last-error.md)

- [PHP Manual](index.md)
- [Функції libxml](ref.libxml.md)
- Отримання масиву помилок, що відбулися

# libxml_get_errors

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

libxml_get_errors — Отримання масиву помилок, що відбулися.

### Опис

**libxml_get_errors**(): array

Отримання масиву помилок, що відбулися.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив об'єктів [LibXMLError](class.libxmlerror.md), якщо в
Буфер є помилки, або порожній масив в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **libxml_get_errors()****

Цей приклад демонструє, як створити простий обробник помилок libxml.

` <?phplibxml_use_internal_errors(true);$xmlstr = <<< XML<?xml version='1.0' standalone='yes'?><movies> <movie>  <titles>PHP: Behind the Parser</tit movie></movies>XML;$doc = simplexml_load_string($xmlstr);$xml = explode("
", $xmlstr);if ($doc === false) {    $errors = libxml_get_errors();    foreach ($errors as $error) {        echo display_xml_error($error, $xml);    }    libxml_clear_errors();}function display_xml_error ($error, $xml){    $return  = $xml[$error->line - 1] . "
";   $return .= str_repeat('-', $error->column) . "^
";    switch ($error->level) {        case LIBXML_ERR_WARNING:            $return .= "Warning $error->code: ";            break;         case LIBXML_ERR_ERROR:            $return .= "Error $error->code: ";            break;        case LIBXML_ERR_FATAL:            $return .= "Fatal Error $error->code: ";            break;    }    $return .= trim($error->message) .               "
Line: $error->line" .                "
Column: $error->column";
File: $error->file";    }    return "$return

--------------------------------------------

";}?> `

Результат виконання цього прикладу:

<titles>PHP: Behind the Parser</title>
----------------------------------------------^
Fatal Error 76: Opening та ending tag mismatch: titles line 4 and title
Line: 4
Column: 46

--------------------------------------------

### Дивіться також

- [libxml_get_last_error()](function.libxml-get-last-error.md) -
Вилучення останньої помилки з libxml
- [libxml_clear_errors()](function.libxml-clear-errors.md) - Очистка
буфер помилок libxml
