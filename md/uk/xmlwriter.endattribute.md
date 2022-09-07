---
navigation:
  - class.xmlwriter.md: « XMLWriter
  - xmlwriter.endcdata.md: 'XMLWriter::endCdata »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endAttribute'
---
# XMLWriter::endAttribute

# xmlwriterendattribute

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endAttribute -- xmlwriterendattribute — Завершити атрибут

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startAttribute()](xmlwriter.startattribute.md) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.md) - Створити стартовий атрибут простору імен
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.md) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.md) - Записати повний атрибут простору імен
