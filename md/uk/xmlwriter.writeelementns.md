---
navigation:
  - xmlwriter.writeelement.md: '« XMLWriter::writeElement'
  - xmlwriter.writepi.md: 'XMLWriter::writePi »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeElementNs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeElementNs

# xmlwriter\_write\_element\_ns

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeElementNs -- xmlwriter\_write\_element\_ns — Записати повний простір імен тега елемента

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeElementNs(    ?string $prefix,    string $name,    ?string $namespace,    ?string $content = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_element_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace,    ?string $content = null): bool
```

Записує повний простір імен тега елемента.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`prefix`

Префікс простору імен. Якщо `prefix`равен\*\*`null`\*\*, простір імен буде опущено.

`name`

Ім'я елемент.

`namespace`

URI простір імен. Якщо `namespace`равен\*\*`null`\*\*, оголошення простору імен буде опущено.

`content`

Вміст елемента.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElementNs()](xmlwriter.startelementns.md) \- Створити стартовий тег елемента простору імен
-   [XMLWriter::endElement()](xmlwriter.endelement.md) \- Завершити поточний елемент
-   [XMLWriter::writeElement()](xmlwriter.writeelement.md) \- Записати повний тег елемента
