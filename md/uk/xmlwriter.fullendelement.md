---
navigation:
  - xmlwriter.flush.md: '« XMLWriter::flush'
  - xmlwriter.openmemory.md: 'XMLWriter::openMemory »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::fullEndElement'
---
# XMLWriter::fullEndElement

# xmlwriterfullendelement

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL xmlwriter >= 2.0.4)

XMLWriter::fullEndElement -- xmlwriterfullendelement — Завершити поточний елемент

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endElement()](xmlwriter.endelement.md) - Завершити поточний елемент
