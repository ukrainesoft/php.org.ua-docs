---
navigation:
  - xmlwriter.enddtd.md: '« XMLWriter::endDtd'
  - xmlwriter.enddtdelement.md: 'XMLWriter::endDtdElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endDtdAttlist'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::endDtdAttlist

# xmlwriter\_end\_dtd\_attlist

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtdAttlist -- xmlwriter\_end\_dtd\_attlist — Завершити поточний список атрибутів DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtdAttlist(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd_attlist(XMLWriter $writer): bool
```

Завершує поточний список атрибутів DTD документа.

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

-   [XMLWriter::startDtdAttlist()](xmlwriter.startdtdattlist.md) \- Створює стартовий список атрибутів DTD
-   [XMLWriter::writeDtdAttlist()](xmlwriter.writedtdattlist.md) \- Записати повний тег DTD AttList
