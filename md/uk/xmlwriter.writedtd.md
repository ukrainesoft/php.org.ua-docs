---
navigation:
  - xmlwriter.writecomment.md: '« XMLWriter::writeComment'
  - xmlwriter.writedtdattlist.md: 'XMLWriter::writeDtdAttlist »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeDtd'
---
# XMLWriter::writeDtd

# xmlwriterwritedtd

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtd -- xmlwriterwritedtd — Записати повний тег DTD

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Ім'я DTD.

`publicId`

Ідентифікатор зовнішнього громадського підмножини.

`systemId`

Ідентифікатор зовнішнього системного підмножини.

`content`

Вміст DTD.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtd()](xmlwriter.startdtd.md) - Створити стартовий DTD тег
-   [XMLWriter::endDtd()](xmlwriter.enddtd.md) - Завершити поточний DTD
