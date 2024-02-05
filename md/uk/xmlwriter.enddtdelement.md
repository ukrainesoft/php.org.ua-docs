---
navigation:
  - xmlwriter.enddtdattlist.md: '« XMLWriter::endDtdAttlist'
  - xmlwriter.enddtdentity.md: 'XMLWriter::endDtdEntity »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::endDtdElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::endDtdElement

# xmlwriter\_end\_dtd\_element

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtdElement -- xmlwriter\_end\_dtd\_element — Завершити поточний елемент DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtdElement(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd_element(XMLWriter $writer): bool
```

Завершує поточний елемент DTD.

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

-   [XMLWriter::startDtdElement()](xmlwriter.startdtdelement.md) \- Створити стартовий елемент DTD
-   [XMLWriter::writeDtdElement()](xmlwriter.writedtdelement.md) \- Записати повний тег елемента DTD
