---
navigation:
  - xmlwriter.startcdata.md: '« XMLWriter::startCdata'
  - xmlwriter.startdocument.md: 'XMLWriter::startDocument »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startComment'
---
# XMLWriter::startComment

# xmlwriterstartcomment

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 1.0.0)

XMLWriter::startComment -- xmlwriterstartcomment — Створює стартовий коментар

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endComment()](xmlwriter.endcomment.md) - Завершити коментар
-   [XMLWriter::writeComment()](xmlwriter.writecomment.md) - Записати повний тег коментаря
