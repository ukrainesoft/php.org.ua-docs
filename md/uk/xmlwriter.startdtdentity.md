---
navigation:
  - xmlwriter.startdtdelement.md: '« XMLWriter::startDtdElement'
  - xmlwriter.startelement.md: 'XMLWriter::startElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startDtdEntity'
---
# XMLWriter::startDtdEntity

# xmlwriterstartdtdentity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtdEntity - xmlwriterstartdtdentity — Створити стартовий запис DTD

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Назва запису.

`isParam`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdEntity()](xmlwriter.enddtdentity.md) - Завершити поточний запис DTD
-   [XMLWriter::writeDtdEntity()](xmlwriter.writedtdentity.md) - Записати повний тег DTD запису
