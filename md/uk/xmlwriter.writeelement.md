---
navigation:
  - xmlwriter.writedtdentity.md: '« XMLWriter::writeDtdEntity'
  - xmlwriter.writeelementns.md: 'XMLWriter::writeElementNs »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeElement'
---
# XMLWriter::writeElement

# xmlwriterwriteelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeElement -- xmlwriterwriteelement — Записати повний тег елемента

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Ім'я елемент.

`content`

Вміст елемента.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElement()](xmlwriter.startelement.md) - Створити стартовий тег елемента
-   [XMLWriter::endElement()](xmlwriter.endelement.md) - Завершити поточний елемент
-   [XMLWriter::writeElementNs()](xmlwriter.writeelementns.md) - Записати повний простір імен тега елемента
