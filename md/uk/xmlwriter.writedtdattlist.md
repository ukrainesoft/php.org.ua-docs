---
navigation:
  - xmlwriter.writedtd.md: '« XMLWriter::writeDtd'
  - xmlwriter.writedtdelement.md: 'XMLWriter::writeDtdElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeDtdAttlist'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeDtdAttlist

# xmlwriter\_write\_dtd\_attlist

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtdAttlist -- xmlwriter\_write\_dtd\_attlist — Записати повний тег DTD AttList

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtdAttlist(string $name, string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd_attlist(XMLWriter $writer, string $name, string $content): bool
```

Записує атрибути DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Назва списку атрибутів DTD.

`content`

Вміст списку атрибутів DTD.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdAttlist()](xmlwriter.startdtdattlist.md) \- Створює стартовий список атрибутів DTD
-   [XMLWriter::endDtdAttlist()](xmlwriter.enddtdattlist.md) \- Завершити поточний список атрибутів DTD
