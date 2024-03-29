---
navigation:
  - xmlwriter.writedtdelement.md: '« XMLWriter::writeDtdElement'
  - xmlwriter.writeelement.md: 'XMLWriter::writeElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeDtdEntity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeDtdEntity

# xmlwriter\_write\_dtd\_entity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtdEntity -- xmlwriter\_write\_dtd\_entity — Записати повний тег DTD запису

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtdEntity(    string $name,    string $content,    bool $isParam = false,    ?string $publicId = null,    ?string $systemId = null,    ?string $notationData = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd_entity(    XMLWriter $writer,    string $name,    string $content,    bool $isParam = false,    ?string $publicId = null,    ?string $systemId = null,    ?string $notationData = null): bool
```

Записує повний запис DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Назва запису.

`content`

Вміст запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |
| 8.0.0 | `publicId` `systemId`и`notationData` тепер допускають значення null. |

### Дивіться також

-   [XMLWriter::startDtdEntity()](xmlwriter.startdtdentity.md) \- Створити стартовий запис DTD
-   [XMLWriter::endDtdEntity()](xmlwriter.enddtdentity.md) \- Завершити поточний запис DTD
