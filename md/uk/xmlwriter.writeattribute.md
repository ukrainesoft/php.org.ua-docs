---
navigation:
  - xmlwriter.text.md: '« XMLWriter::text'
  - xmlwriter.writeattributens.md: 'XMLWriter::writeAttributeNs »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeAttribute'
---
# XMLWriter::writeAttribute

# xmlwriterwriteattribute

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeAttribute -- xmlwriterwriteattribute — Записати повний атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeAttribute(string $name, string $value): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_attribute(XMLWriter $writer, string $name, string $value): bool
```

Записує повний атрибут.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Ім'я атрибуту.

`value`

Значення атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Перемішування поделементів та атрибутів**

Якщо запис поделементів та атрибутів змішаний, будь-яка спроба запису атрибутів після першого поделемента завершиться помилкою і поверне false.

```php
<?php
$xml = new XMLWriter();
$xml->openMemory();

$xml->startElement('element');
$xml->writeAttribute('attr1', '0');
$xml->writeElement('subelem', '0');
var_dump($xml->writeAttribute('attr2', '0'));
$xml->endElement();

echo $xml->flush();
?>
```

Результат виконання цього прикладу:

```
bool(false)
<element attr1="0"><subelem>0</subelem></element>
```

### Дивіться також

-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.md) - Записати повний атрибут простору імен
-   [XMLWriter::startAttribute()](xmlwriter.startattribute.md) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.md) - Створити стартовий атрибут простору імен
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.md) - Завершити атрибут
