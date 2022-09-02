---
navigation:
  - xmlwriter.writecdata.md: '« XMLWriter::writeCdata'
  - xmlwriter.writedtd.md: 'XMLWriter::writeDtd »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeComment'
---
# XMLWriter::writeComment

# xmlwriterwritecomment

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeComment -- xmlwriterwritecomment — Записати повний тег коментаря

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeComment(string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_comment(XMLWriter $writer, string $content): bool
```

Записує повний коментар.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`content`

Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startComment()](xmlwriter.startcomment.md) - Створює стартовий коментар
-   [XMLWriter::endComment()](xmlwriter.endcomment.md) - Завершити коментар
