---
navigation:
  - xmlwriter.startdtdattlist.md: '« XMLWriter::startDtdAttlist'
  - xmlwriter.startdtdentity.md: 'XMLWriter::startDtdEntity »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startDtdElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startDtdElement

# xmlwriter\_start\_dtd\_element

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtdElement -- xmlwriter\_start\_dtd\_element — Створити стартовий елемент DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtdElement(string $qualifiedName): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd_element(XMLWriter $writer, string $qualifiedName): bool
```

Починає елемент DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`qualifiedName`

Цілком визначене ім'я типу документа для створення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdElement()](xmlwriter.enddtdelement.md) \- Завершити поточний елемент DTD
-   [XMLWriter::writeDtdElement()](xmlwriter.writedtdelement.md) \- Записати повний тег елемента DTD
