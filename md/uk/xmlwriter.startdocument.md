---
navigation:
  - xmlwriter.startcomment.md: '« XMLWriter::startComment'
  - xmlwriter.startdtd.md: 'XMLWriter::startDtd »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startDocument'
---
# XMLWriter::startDocument

# xmlwriterstartdocument

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDocument -- xmlwriterstartdocument — Створити тег документа

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`version`

Номер версії документа як частина оголошення XML.

`encoding`

Кодування документа як частину об'яви XML.

`standalone`

`yes` або `no`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDocument()](xmlwriter.enddocument.md) - Завершити поточний документ
