---
navigation:
  - xmlwriter.endcomment.md: '« XMLWriter::endComment'
  - xmlwriter.enddtd.md: 'XMLWriter::endDtd »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endDocument'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::endDocument

# xmlwriter\_end\_document

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDocument -- xmlwriter\_end\_document — Завершити поточний документ

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDocument(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_document(XMLWriter $writer): bool
```

Завершує поточний документ.

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

-   [XMLWriter::startDocument()](xmlwriter.startdocument.md) \- Створити тег документа
