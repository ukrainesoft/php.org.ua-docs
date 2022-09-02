---
navigation:
  - xmlwriter.startattributens.md: '« XMLWriter::startAttributeNs'
  - xmlwriter.startcomment.md: 'XMLWriter::startComment »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startCdata'
---
# XMLWriter::startCdata

# xmlwriterstartcdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startCdata -- xmlwriterstartcdata — Створити початковий тег CDATA

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endCdata()](xmlwriter.endcdata.md) - Завершити поточну секцію CDATA
-   [XMLWriter::writeCdata()](xmlwriter.writecdata.md) - Записати повний тег CDATA
