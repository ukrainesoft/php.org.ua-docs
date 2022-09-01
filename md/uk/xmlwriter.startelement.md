---
navigation:
  - xmlwriter.startdtdentity.md: '« XMLWriter::startDtdEntity'
  - xmlwriter.startelementns.md: 'XMLWriter::startElementNs »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startElement'
---
# XMLWriter::startElement

# xmlwriterstartelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startElement -- xmlwriterstartelement — Створити стартовий тег елемента

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Ім'я елемент.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endElement()](xmlwriter.endelement.md) - Завершити поточний елемент
-   [XMLWriter::writeElement()](xmlwriter.writeelement.md) - Записати повний тег елемента
