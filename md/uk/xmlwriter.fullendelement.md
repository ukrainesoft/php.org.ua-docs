---
navigation:
  - xmlwriter.flush.md: '« XMLWriter::flush'
  - xmlwriter.openmemory.md: 'XMLWriter::openMemory »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::fullEndElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::fullEndElement

# xmlwriter\_full\_end\_element

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL xmlwriter >= 2.0.4)

XMLWriter::fullEndElement -- xmlwriter\_full\_end\_element — Завершити поточний елемент

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::fullEndElement(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_full_end_element(XMLWriter $writer): bool
```

Завершує поточний елемент XML. Записує тег, що закриває, навіть якщо елемент порожній.

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

-   [XMLWriter::endElement()](xmlwriter.endelement.md) \- Завершити поточний елемент
