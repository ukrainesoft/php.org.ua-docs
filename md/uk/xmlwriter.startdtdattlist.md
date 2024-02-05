---
navigation:
  - xmlwriter.startdtd.md: '« XMLWriter::startDtd'
  - xmlwriter.startdtdelement.md: 'XMLWriter::startDtdElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startDtdAttlist'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startDtdAttlist

# xmlwriter\_start\_dtd\_attlist

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtdAttlist -- xmlwriter\_start\_dtd\_attlist — Створення стартового списку атрибутів DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtdAttlist(string $name): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd_attlist(XMLWriter $writer, string $name): bool
```

Починає перелік атрибутів DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Назва списку атрибутів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdAttlist()](xmlwriter.enddtdattlist.md) \- Завершити поточний список атрибутів DTD
-   [XMLWriter::writeDtdAttlist()](xmlwriter.writedtdattlist.md) \- Записати повний тег DTD AttList
