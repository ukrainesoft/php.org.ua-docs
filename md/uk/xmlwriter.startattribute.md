---
navigation:
  - xmlwriter.setindentstring.md: '« XMLWriter::setIndentString'
  - xmlwriter.startattributens.md: 'XMLWriter::startAttributeNs »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startAttribute'
---
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад базового використання **XMLWriter::startAttribute()****

```php
<?php
$writer = new XMLWriter;
$writer->openURI('php://output');
$writer->startDocument('1.0', 'UTF-8');
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

-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.md) - Створити стартовий атрибут простору імен
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.md) - Завершити атрибут
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.md) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.md) - Записати повний атрибут простору імен
