---
navigation:
  - function.xml-parse.md: « xml\_parse
  - function.xml-parser-create.md: xml\_parser\_create »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_parser\_create\_ns
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_parser\_create\_ns

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

xml\_parser\_create\_ns — Створення XML-аналізатора з підтримкою просторів імен

### Опис

```methodsynopsis
xml_parser_create_ns(?string $encoding = null, string $separator = ":"): XMLParser
```

**xml\_parser\_create\_ns()** створює новий синтаксичний XML-аналізатор з підтримкою простору імен та повертає екземпляр [XMLParser](class.xmlparser.md), який буде використовуватися в інших функціях XML.

### Список параметрів

`encoding`

Кодування вхідних даних визначається автоматично, а `encoding` задає кодування тільки для даних, що виводяться. Якщо передається порожній рядок, аналізатор спробує визначити кодування, переглядаючи перші 3 або 4 байти. Стандартне кодування - UTF-8. Список підтримуваних кодувань: `ISO-8859-1` `UTF-8`и`US-ASCII`

`separator`

Якщо повідомити аналізатору простір імен, то параметри тегів, що передаються в різні обробники, будуть складатися з простору імен та локального імені, відокремлених заданим у цьому аргументі роздільником `separator`

### Значення, що повертаються

Повертає новий екземпляр [XMLParser](class.xmlparser.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер повертає екземпляр [XMLParser](class.xmlparser.md); раніше повертався ресурс (resource) або \*\*`false`\*\*в случае возникновения ошибки. |
| 8.0.0 | `encoding` тепер допускає значення null. |

### Дивіться також

-   [xml\_parser\_create()](function.xml-parser-create.md) \- Створення XML-аналізатора
-   [xml\_parser\_free()](function.xml-parser-free.md) \- Звільнення XML-аналізатора
