---
navigation:
  - xmlwriter.startcdata.md: '« XMLWriter::startCdata'
  - xmlwriter.startdocument.md: 'XMLWriter::startDocument »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startComment

# xmlwriter\_start\_comment

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 1.0.0)

XMLWriter::startComment -- xmlwriter\_start\_comment — Створює стартовий коментар

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startComment(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_comment(XMLWriter $writer): bool
```

Починає коментар.

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

-   [XMLWriter::endComment()](xmlwriter.endcomment.md) \- Завершити коментар
-   [XMLWriter::writeComment()](xmlwriter.writecomment.md) \- Записати повний тег коментаря
