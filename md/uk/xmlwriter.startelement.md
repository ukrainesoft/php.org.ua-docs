---
navigation:
  - xmlwriter.startdtdentity.md: '« XMLWriter::startDtdEntity'
  - xmlwriter.startelementns.md: 'XMLWriter::startElementNs »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startElement

# xmlwriter\_start\_element

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startElement -- xmlwriter\_start\_element — Створити стартовий тег елемента

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startElement(string $name): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_element(XMLWriter $writer, string $name): bool
```

Починає елемент.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Ім'я елемент.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endElement()](xmlwriter.endelement.md) \- Завершити поточний елемент
-   [XMLWriter::writeElement()](xmlwriter.writeelement.md) \- Записати повний тег елемента
