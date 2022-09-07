---
navigation:
  - function.xml-parse.md: « xmlparse
  - function.xml-parser-create.md: xmlparsercreate »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlparsercreateнс
---
# xmlparsercreateнс

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

xmlparsercreatens — Створення XML-аналізатора за допомогою просторів імен

### Опис

```methodsynopsis
xml_parser_create_ns(?string $encoding = null, string $separator = ":"): XMLParser
```

**xmlparsercreatens()** створює новий синтаксичний XML-аналізатор з підтримкою простору імен та повертає екземпляр [XMLParser](class.xmlparser.md), який використовуватиметься в інших XML-функціях.

### Список параметрів

`encoding`

Кодування вхідних даних визначається автоматично, а `encoding` задає кодування тільки для даних, що виводяться. Якщо передається порожній рядок, аналізатор спробує визначити кодування, переглядаючи перші 3 або 4 байти. Стандартне кодування - UTF-8. Список підтримуваних кодувань: `ISO-8859-1` `UTF-8` і `US-ASCII`

`separator`

Якщо повідомити аналізатору простір імен, то параметри тегів, що передаються в різні обробники, будуть складатися з простору імен та локального імені, відокремлених заданим у цьому аргументі роздільником `separator`

### Значення, що повертаються

Повертає новий екземпляр [XMLParser](class.xmlparser.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер повертає екземпляр [XMLParser](class.xmlparser.md); раніше повертався ресурс (resource) або **`false`** у разі виникнення помилки. |
|  | `encoding` тепер допускає значення null. |

### Дивіться також

-   [xmlparsercreate()](function.xml-parser-create.md) - Створення XML-аналізатора
-   [xmlparserfree()](function.xml-parser-free.md) - Звільнення XML-аналізатора
