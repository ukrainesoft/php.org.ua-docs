---
navigation:
  - xmlwriter.endcdata.md: '« XMLWriter::endCdata'
  - xmlwriter.enddocument.md: 'XMLWriter::endDocument »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endComment'
---
# XMLWriter::endComment

# xmlwriterendcomment

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 1.0.0)

XMLWriter::endComment -- xmlwriterendcomment — Завершити коментар

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endComment(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_comment(XMLWriter $writer): bool
```

Завершує поточний коментар.

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

-   [XMLWriter::startComment()](xmlwriter.startcomment.md) - Створює стартовий коментар
-   [XMLWriter::writeComment()](xmlwriter.writecomment.md) - Записати повний тег коментаря
