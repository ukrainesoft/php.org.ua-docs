---
navigation:
  - xmlwriter.startcomment.md: '« XMLWriter::startComment'
  - xmlwriter.startdtd.md: 'XMLWriter::startDtd »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startDocument'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startDocument

# xmlwriter\_start\_document

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDocument -- xmlwriter\_start\_document — Створити тег документа

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDocument(?string $version = "1.0", ?string $encoding = null, ?string $standalone = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_document(    XMLWriter $writer,    ?string $version = "1.0",    ?string $encoding = null,    ?string $standalone = null): bool
```

Починає документ.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`version`

Номер версії документа як частина оголошення XML.

`encoding`

Кодування документа як частину об'яви XML.

`standalone`

`yes`или`no`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDocument()](xmlwriter.enddocument.md) \- Завершити поточний документ
