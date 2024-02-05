---
navigation:
  - xmlwriter.enddocument.md: '« XMLWriter::endDocument'
  - xmlwriter.enddtdattlist.md: 'XMLWriter::endDtdAttlist »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endDtd'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::endDtd

# xmlwriter\_end\_dtd

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtd -- xmlwriter\_end\_dtd — Завершити поточний DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtd(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd(XMLWriter $writer): bool
```

Завершує розділ визначення типу документа (DTD).

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

-   [XMLWriter::startDtd()](xmlwriter.startdtd.md) \- Створити стартовий DTD тег
-   [XMLWriter::writeDtd()](xmlwriter.writedtd.md) \- Записати повний тег DTD
