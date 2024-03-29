---
navigation:
  - simplexml.examples-basic.md: « Базове використання SimpleXML
  - class.simplexmlelement.md: SimpleXMLElement »
  - index.md: PHP Manual
  - simplexml.examples.md: Приклади
title: Робота з помилками XML
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Робота з помилками XML

Робота з помилками XML під час завантаження документів є дуже простим завданням. Використання функціональності [libxml](book.libxml.md) дозволяє придушити всі помилки XML під час завантаження документа і потім обробити їх.

Об'єкт [libXMLError](class.libxmlerror.md), що повертається [libxml\_get\_errors()](function.libxml-get-errors.md)містить кілька властивостей, у тому числі [повідомлення](class.libxmlerror.md#libxmlerror.props.message) [номер рядка](class.libxmlerror.md#libxmlerror.props.line) і [колонку](class.libxmlerror.md#libxmlerror.props.column) (Позицію) цієї помилки.

**Приклад #1 Завантаження синтаксично неправильного рядка XML**

```php
<?php
libxml_use_internal_errors(true);
$sxe = simplexml_load_string("<?xml version='1.0'><broken><xml></broken>");
if (!$sxe) {
    echo "Ошибка загрузки XML\n";
    foreach(libxml_get_errors() as $error) {
        echo "\t", $error->message;
    }
}
?>
```

Результат виконання наведеного прикладу:

```
Ошибка загрузки XML
    Blank needed here
    parsing XML declaration: '?>' expected
    Opening and ending tag mismatch: xml line 1 and broken
    Premature end of data in tag broken line 1
```

## Дивіться також

-   [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.md)
-   [libxml\_get\_errors()](function.libxml-get-errors.md)
-   [LibXMLError](class.libxmlerror.md)
