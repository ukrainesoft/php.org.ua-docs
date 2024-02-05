---
navigation:
  - xmlwriter.writedtdentity.md: '« XMLWriter::writeDtdEntity'
  - xmlwriter.writeelementns.md: 'XMLWriter::writeElementNs »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeElement

# xmlwriter\_write\_element

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeElement -- xmlwriter\_write\_element — Записати повний тег елемента

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeElement(string $name, ?string $content = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_element(XMLWriter $writer, string $name, ?string $content = null): bool
```

Записує повний тег елемент.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`name`

Ім'я елемент.

`content`

Вміст елемента.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElement()](xmlwriter.startelement.md) \- Створити стартовий тег елемента
-   [XMLWriter::endElement()](xmlwriter.endelement.md) \- Завершити поточний елемент
-   [XMLWriter::writeElementNs()](xmlwriter.writeelementns.md) \- Записати повний простір імен тега елемента
