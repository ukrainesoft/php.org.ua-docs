---
navigation:
  - xmlwriter.startattribute.md: '« XMLWriter::startAttribute'
  - xmlwriter.startcdata.md: 'XMLWriter::startCdata »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startAttributeNs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startAttributeNs

# xmlwriter\_start\_attribute\_ns

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startAttributeNs -- xmlwriter\_start\_attribute\_ns — Створити стартовий атрибут простору імен

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startAttributeNs(?string $prefix, string $name, ?string $namespace): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_attribute_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace): bool
```

Починає атрибут простору імен.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`prefix`

Префікс простору імен.

`name`

Ім'я атрибуту.

`namespace`

URI простір імен. Якщо `namespace`равен\*\*`null`\*\*, оголошення простору імен буде опущено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |
| 8.0.0 | `prefix` тепер допускає значення null. |

### Дивіться також

-   [XMLWriter::startAttribute()](xmlwriter.startattribute.md) \- Створити початковий атрибут
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.md) \- Завершити атрибут
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.md) \- Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.md) \- Записати повний атрибут простору імен
