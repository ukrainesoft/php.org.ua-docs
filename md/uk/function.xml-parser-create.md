---
navigation:
  - function.xml-parser-create-ns.md: « xmlparsercreateнс
  - function.xml-parser-free.md: xmlparserfree »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlparsercreate
---
# xmlparsercreate

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlparsercreate — Створення XML-аналізатора

### Опис

```methodsynopsis
xml_parser_create(?string $encoding = null): XMLParser
```

**xmlparsercreate()** створює новий XML-аналізатор та повертає екземпляр [XMLParser](class.xmlparser.md), який можна використовувати в інших функціях XML.

### Список параметрів

`encoding`

Кодування вхідних даних визначається автоматично, а параметр `encoding` задає кодування тільки для даних, що виводяться. Якщо передається порожній рядок, аналізатор спробує визначити кодування, переглядаючи перші 3 або 4 байти. Стандартне кодування - UTF-8. Список підтримуваних кодувань: `ISO-8859-1` `UTF-8` і `US-ASCII`

### Значення, що повертаються

Повертає новий екземпляр [XMLParser](class.xmlparser.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер повертає екземпляр [XMLParser](class.xmlparser.md); раніше повертався ресурс (resource) або **`false`** у разі виникнення помилки. |
|  | `encoding` тепер допускає значення null. |

### Дивіться також

-   [xmlparsercreatens()](function.xml-parser-create-ns.md) - Створення XML-аналізатора з підтримкою просторів імен
-   [xmlparserfree()](function.xml-parser-free.md) - Звільнення XML-аналізатора
