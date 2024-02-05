---
navigation:
  - xmlwriter.startattributens.md: '« XMLWriter::startAttributeNs'
  - xmlwriter.startcomment.md: 'XMLWriter::startComment »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startCdata'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startCdata

# xmlwriter\_start\_cdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startCdata -- xmlwriter\_start\_cdata — Створити початковий тег CDATA

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startCdata(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_cdata(XMLWriter $writer): bool
```

Починає CDATA.

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

-   [XMLWriter::endCdata()](xmlwriter.endcdata.md) \- Завершити поточну секцію CDATA
-   [XMLWriter::writeCdata()](xmlwriter.writecdata.md) \- Записати повний тег CDATA
