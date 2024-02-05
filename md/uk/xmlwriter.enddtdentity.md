---
navigation:
  - xmlwriter.enddtdelement.md: '« XMLWriter::endDtdElement'
  - xmlwriter.endelement.md: 'XMLWriter::endElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endDtdEntity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::endDtdEntity

# xmlwriter\_end\_dtd\_entity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtdEntity -- xmlwriter\_end\_dtd\_entity — Завершити поточний запис DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtdEntity(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd_entity(XMLWriter $writer): bool
```

Завершує поточний запис DTD.

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

-   [XMLWriter::startDtdEntity()](xmlwriter.startdtdentity.md) \- Створити стартовий запис DTD
-   [XMLWriter::writeDtdEntity()](xmlwriter.writedtdentity.md) \- Записати повний тег DTD запису
