---
navigation:
  - xmlwriter.writecomment.md: '« XMLWriter::writeComment'
  - xmlwriter.writedtdattlist.md: 'XMLWriter::writeDtdAttlist »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeDtd'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeDtd

# xmlwriter\_write\_dtd

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtd -- xmlwriter\_write\_dtd — Записати повний тег DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtd(    string $name,    ?string $publicId = null,    ?string $systemId = null,    ?string $content = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd(    XMLWriter $writer,    string $name,    ?string $publicId = null,    ?string $systemId = null,    ?string $content = null): bool
```

Записує повний тег DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Ім'я DTD.

`publicId`

Ідентифікатор зовнішнього громадського підмножини.

`systemId`

Ідентифікатор зовнішнього системного підмножини.

`content`

Вміст DTD.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtd()](xmlwriter.startdtd.md) \- Створити стартовий DTD тег
-   [XMLWriter::endDtd()](xmlwriter.enddtd.md) \- Завершити поточний DTD
