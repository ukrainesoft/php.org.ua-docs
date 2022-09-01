---
navigation:
  - xmlwriter.writecdata.html: '« XMLWriter::writeCdata'
  - xmlwriter.writedtd.html: 'XMLWriter::writeDtd »'
  - index.html: PHP Manual
  - class.xmlwriter.html: XMLWriter
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`content`

Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startComment()](xmlwriter.startcomment.html) - Створює стартовий коментар
-   [XMLWriter::endComment()](xmlwriter.endcomment.html) - Завершити коментар
