---
navigation:
  - xmlwriter.endcomment.md: '« XMLWriter::endComment'
  - xmlwriter.enddtd.md: 'XMLWriter::endDtd »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endDocument'
---
# XMLWriter::endDocument

# xmlwriterenddocument

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDocument -- xmlwriterenddocument — Завершити поточний документ

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDocument()](xmlwriter.startdocument.md) - Створити тег документа
