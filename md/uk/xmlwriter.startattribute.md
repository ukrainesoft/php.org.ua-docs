---
navigation:
  - xmlwriter.setindentstring.md: '« XMLWriter::setIndentString'
  - xmlwriter.startattributens.md: 'XMLWriter::startAttributeNs »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startAttribute

# xmlwriter\_start\_attribute

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startAttribute -- xmlwriter\_start\_attribute - Створити початковий атрибут

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад базового использования**XMLWriter::startAttribute()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
<?xml version="1.0" encoding="UTF-8"?>
<element attribute="value"/>
```

### Дивіться також

-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.md) \- Створити стартовий атрибут простору імен
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.md) \- Завершити атрибут
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.md) \- Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.md) \- Записати повний атрибут простору імен
