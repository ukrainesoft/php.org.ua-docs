---
navigation:
  - xmlwriter.startdocument.md: '« XMLWriter::startDocument'
  - xmlwriter.startdtdattlist.md: 'XMLWriter::startDtdAttlist »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startDtd'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startDtd

# xmlwriter\_start\_dtd

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtd -- xmlwriter\_start\_dtd - Створити стартовий DTD тег

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtd(string $qualifiedName, ?string $publicId = null, ?string $systemId = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd(    XMLWriter $writer,    string $qualifiedName,    ?string $publicId = null,    ?string $systemId = null): bool
```

Починає DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`qualifiedName`

Цілком визначене ім'я типу документа для створення.

`publicId`

Ідентифікатор зовнішнього громадського підмножини.

`systemId`

Ідентифікатор зовнішнього системного підмножини.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtd()](xmlwriter.enddtd.md) \- Завершити поточний DTD
-   [XMLWriter::writeDtd()](xmlwriter.writedtd.md) \- Записати повний тег DTD
