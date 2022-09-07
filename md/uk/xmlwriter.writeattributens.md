---
navigation:
  - xmlwriter.writeattribute.md: '« XMLWriter::writeAttribute'
  - xmlwriter.writecdata.md: 'XMLWriter::writeCdata »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeAttributeNs'
---
# XMLWriter::writeAttributeNs

# xmlwriterwriteattributeнс

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeAttributeNs -- xmlwriterwriteattributens — Записати повний атрибут простору імен

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeAttributeNs(    ?string $prefix,    string $name,    ?string $namespace,    string $value): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_attribute_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace,    string $value): bool
```

Записує повний атрибут простору імен.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`prefix`

Префікс простору імен. Якщо `prefix` дорівнює **`null`**, простір імен буде опущено.

`name`

Ім'я атрибуту.

`namespace`

URI простір імен. Якщо `namespace` дорівнює **`null`**, оголошення простору імен буде опущено.

`content`

Значення атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.md) - Записати повний атрибут
-   [XMLWriter::startAttribute()](xmlwriter.startattribute.md) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.md) - Створити стартовий атрибут простору імен
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.md) - Завершити атрибут
