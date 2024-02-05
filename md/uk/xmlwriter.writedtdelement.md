---
navigation:
  - xmlwriter.writedtdattlist.md: '« XMLWriter::writeDtdAttlist'
  - xmlwriter.writedtdentity.md: 'XMLWriter::writeDtdEntity »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeDtdElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeDtdElement

# xmlwriter\_write\_dtd\_element

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtdElement -- xmlwriter\_write\_dtd\_element — Записати повний тег елемента DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtdElement(string $name, string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd_element(XMLWriter $writer, string $name, string $content): bool
```

Записує повний тег елемента DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Назва елемента DTD.

`content`

Вміст елемента.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdElement()](xmlwriter.startdtdelement.md) \- Створити стартовий елемент DTD
-   [XMLWriter::endDtdElement()](xmlwriter.enddtdelement.md) \- Завершити поточний елемент DTD
