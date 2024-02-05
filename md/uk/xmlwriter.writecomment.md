---
navigation:
  - xmlwriter.writecdata.md: '« XMLWriter::writeCdata'
  - xmlwriter.writedtd.md: 'XMLWriter::writeDtd »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeComment

# xmlwriter\_write\_comment

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeComment -- xmlwriter\_write\_comment — Записати повний тег коментаря

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`content`

Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startComment()](xmlwriter.startcomment.md) \- Створює стартовий коментар
-   [XMLWriter::endComment()](xmlwriter.endcomment.md) \- Завершити коментар
