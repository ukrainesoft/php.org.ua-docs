---
navigation:
  - class.xmlwriter.md: « XMLWriter
  - xmlwriter.endcdata.md: 'XMLWriter::endCdata »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::endAttribute

# xmlwriter\_end\_attribute

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endAttribute -- xmlwriter\_end\_attribute — Завершити атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endAttribute(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_attribute(XMLWriter $writer): bool
```

Завершує поточний атрибут.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startAttribute()](xmlwriter.startattribute.md) \- Створити початковий атрибут
-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.md) \- Створити стартовий атрибут простору імен
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.md) \- Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.md) \- Записати повний атрибут простору імен
