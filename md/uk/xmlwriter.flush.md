---
navigation:
  - xmlwriter.endpi.md: '« XMLWriter::endPi'
  - xmlwriter.fullendelement.md: 'XMLWriter::fullEndElement »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::flush'
---
# XMLWriter::flush

# xmlwriterflush

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 1.0.0)

XMLWriter::flush -- xmlwriterflush — Скинути поточний буфер

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::flush(bool $empty = true): string|int
```

Процедурний стиль

```methodsynopsis
xmlwriter_flush(XMLWriter $writer, bool $empty = true): string|int
```

Скидає поточний буфер.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`empty`

Визначає, чи звільнити буфер чи ні. За замовчуванням **`true`**

### Значення, що повертаються

Якщо XML створюється в пам'яті, функція поверне згенерований буфер XML, інакше, при використанні URI, ця функція запише буфер і поверне кількість записаних байт.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |
|  | Функція більше не може повертати **`false`** |
