---
navigation:
  - xmlwriter.startdtdelement.md: '« XMLWriter::startDtdElement'
  - xmlwriter.startelement.md: 'XMLWriter::startElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startDtdEntity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startDtdEntity

# xmlwriter\_start\_dtd\_entity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtdEntity -- xmlwriter\_start\_dtd\_entity — Створити стартовий запис DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtdEntity(string $name, bool $isParam): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd_entity(XMLWriter $writer, string $name, bool $isParam): bool
```

Починає записування DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Назва запису.

`isParam`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdEntity()](xmlwriter.enddtdentity.md) \- Завершити поточний запис DTD
-   [XMLWriter::writeDtdEntity()](xmlwriter.writedtdentity.md) \- Записати повний тег DTD запису
