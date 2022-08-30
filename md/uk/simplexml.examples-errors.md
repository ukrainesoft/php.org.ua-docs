Робота з помилками XML

-   [« Базовое использование SimpleXML](simplexml.examples-basic.html)
    
-   [SimpleXMLElement »](class.simplexmlelement.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](simplexml.examples.html)
    
-   Робота з помилками XML
    

## Робота з помилками XML

Робота з помилками XML під час завантаження документів є дуже простим завданням. Використання функціональності [libxml](book.libxml.html) дозволяє придушити всі помилки XML під час завантаження документа і потім обробити їх.

Об'єкт [libXMLError](class.libxmlerror.html), що повертається [libxmlgeterrors()](function.libxml-get-errors.html)містить кілька властивостей, у тому числі [сообщение](class.libxmlerror.html#libxmlerror.props.message) [номер рядка](class.libxmlerror.html#libxmlerror.props.line) і [колонку](class.libxmlerror.html#libxmlerror.props.column) (Позицію) цієї помилки.

**Приклад #1 Завантаження синтаксично неправильного рядка XML**

```php
<?php
libxml_use_internal_errors(true);
$sxe = simplexml_load_string("<?xml version='1.0'><broken><xml></broken>");
if (!$sxe) {
    echo "Ошибка загрузки XML\n";
    foreach(libxml_get_errors() as $error) {
        echo "\t", $error->message;
    }
}
?>
```

Результат виконання цього прикладу:

```
Ошибка загрузки XML
    Blank needed here
    parsing XML declaration: '?>' expected
    Opening and ending tag mismatch: xml line 1 and broken
    Premature end of data in tag broken line 1
```

## Дивіться також

-   [libxmluseinternalerrors()](function.libxml-use-internal-errors.html)
-   [libxmlgeterrors()](function.libxml-get-errors.html)
-   [libXMLError](class.libxmlerror.html)