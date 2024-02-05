---
navigation:
  - xmlwriter.startelement.md: '« XMLWriter::startElement'
  - xmlwriter.startpi.md: 'XMLWriter::startPi »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::startElementNs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::startElementNs

# xmlwriter\_start\_element\_ns

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startElementNs -- xmlwriter\_start\_element\_ns — Створити стартовий тег елемента простору імен

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startElementNs(?string $prefix, string $name, ?string $namespace): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_element_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace): bool
```

Починає елемент простору імен.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`prefix`

Префікс простору імен. Якщо `prefix`равен\*\*`null`\*\*, простір імен буде опущено.

`name`

Ім'я елемент.

`namespace`

URI простір імен. Якщо `namespace`равен\*\*`null`\*\*, оголошення простору імен буде опущено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endElement()](xmlwriter.endelement.md) \- Завершити поточний елемент
-   [XMLWriter::writeElementNs()](xmlwriter.writeelementns.md) \- Записати повний простір імен тега елемента
