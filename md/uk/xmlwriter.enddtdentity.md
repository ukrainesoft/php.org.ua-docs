---
navigation:
  - xmlwriter.enddtdelement.md: '« XMLWriter::endDtdElement'
  - xmlwriter.endelement.md: 'XMLWriter::endElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endDtdEntity'
---
# XMLWriter::endDtdEntity

# xmlwriterenddtdentity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtdEntity -- xmlwriterenddtdentity — Завершити поточний запис DTD

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdEntity()](xmlwriter.startdtdentity.md) - Створити стартовий запис DTD
-   [XMLWriter::writeDtdEntity()](xmlwriter.writedtdentity.md) - Записати повний тег DTD запису
