---
navigation:
  - xmlwriter.endattribute.md: '« XMLWriter::endAttribute'
  - xmlwriter.endcomment.md: 'XMLWriter::endComment »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endCdata'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::endCdata

# xmlwriter\_end\_cdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endCdata -- xmlwriter\_end\_cdata — Завершити поточну секцію CDATA

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startCdata()](xmlwriter.startcdata.md) \- Створити початковий тег CDATA
-   [XMLWriter::writeCdata()](xmlwriter.writecdata.md) \- Записати повний тег CDATA
