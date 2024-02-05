---
navigation:
  - function.xml-parser-create-ns.md: « xml\_parser\_create\_ns
  - function.xml-parser-free.md: xml\_parser\_free »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_parser\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_parser\_create

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_parser\_create — Створення XML-аналізатора

### Опис

```methodsynopsis
xml_parser_create(?string $encoding = null): XMLParser
```

**xml\_parser\_create()** створює новий XML-аналізатор та повертає екземпляр [XMLParser](class.xmlparser.md), який можна використовувати в інших функціях XML.

### Список параметрів

`encoding`

Кодування вхідних даних визначається автоматично, а параметр `encoding` задає кодування тільки для даних, що виводяться. Якщо передається порожній рядок, аналізатор спробує визначити кодування, переглядаючи перші 3 або 4 байти. Стандартне кодування - UTF-8. Список підтримуваних кодувань: `ISO-8859-1` `UTF-8`и`US-ASCII`

### Значення, що повертаються

Повертає новий екземпляр [XMLParser](class.xmlparser.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер повертає екземпляр [XMLParser](class.xmlparser.md); раніше повертався ресурс (resource) або \*\*`false`\*\*в случае возникновения ошибки. |
| 8.0.0 | `encoding` тепер допускає значення null. |

### Дивіться також

-   [xml\_parser\_create\_ns()](function.xml-parser-create-ns.md) \- Створення XML-аналізатора з підтримкою просторів імен
-   [xml\_parser\_free()](function.xml-parser-free.md) \- Звільнення XML-аналізатора
