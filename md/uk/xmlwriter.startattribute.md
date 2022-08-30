Створити початковий атрибут

-   [« XMLWriter::setIndentString](xmlwriter.setindentstring.html)
    
-   [XMLWriter::startAttributeNs »](xmlwriter.startattributens.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити початковий атрибут
    

# XMLWriter::startAttribute

# xmlwriterstartattribute

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startAttribute -- xmlwriterstartattribute - Створити початковий атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startAttribute(string $name): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_attribute(XMLWriter $writer, string $name): bool
```

Починає атрибут.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`name`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад базового використання **XMLWriter::startAttribute()****

```php
<?php
$writer = new XMLWriter;
$writer->openURI('php://output');
$writer->startDocument('1.0', 'UTF-8');
$writer->startElement('element');
$writer->startAttribute('attribute');
$writer->text('value');
$writer->endAttribute();
$writer->endElement();
$writer->endDocument();
```

Результатом виконання цього прикладу буде щось подібне:

```
<?xml version="1.0" encoding="UTF-8"?>
<element attribute="value"/>
```

### Дивіться також

-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.html) - Створити стартовий атрибут простору імен
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.html) - Завершити атрибут
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.html) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.html) - Записати повний атрибут простору імен