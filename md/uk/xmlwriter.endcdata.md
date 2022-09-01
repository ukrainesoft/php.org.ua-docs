---
navigation:
  - xmlwriter.endattribute.md: '« XMLWriter::endAttribute'
  - xmlwriter.endcomment.md: 'XMLWriter::endComment »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endCdata'
---
# XMLWriter::endCdata

# xmlwriterendcdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endCdata -- xmlwriterendcdata — Завершити поточну секцію CDATA

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endCdata(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_cdata(XMLWriter $writer): bool
```

Завершує поточну секцію CDATA.

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

-   [XMLWriter::startCdata()](xmlwriter.startcdata.md) - Створити початковий тег CDATA
-   [XMLWriter::writeCdata()](xmlwriter.writecdata.md) - Записати повний тег CDATA
