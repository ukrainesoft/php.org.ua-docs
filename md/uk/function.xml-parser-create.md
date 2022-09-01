---
navigation:
  - function.xml-parser-create-ns.html: « xmlparsercreateнс
  - function.xml-parser-free.html: xmlparserfree »
  - index.html: PHP Manual
  - ref.xml.html: Функции парсера XML
title: xmlparsercreate
---
# xmlparsercreate

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlparsercreate — Створення XML-аналізатора

### Опис

```methodsynopsis
xml_parser_create(?string $encoding = null): XMLParser
```

**xmlparsercreate()** створює новий XML-аналізатор та повертає екземпляр [XMLParser](class.xmlparser.html), який можна використовувати в інших функціях XML.

### Список параметрів

`encoding`

Кодування вхідних даних визначається автоматично, а параметр `encoding` задає кодування тільки для даних, що виводяться. Якщо передається порожній рядок, аналізатор спробує визначити кодування, переглядаючи перші 3 або 4 байти. Стандартне кодування - UTF-8. Список підтримуваних кодувань: `ISO-8859-1` `UTF-8` і `US-ASCII`

### Значення, що повертаються

Повертає новий екземпляр [XMLParser](class.xmlparser.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер повертає екземпляр [XMLParser](class.xmlparser.html); раніше повертався ресурс (resource) або **`false`** у разі виникнення помилки. |
|  | `encoding` тепер допускає значення null. |

### Дивіться також

-   [xmlparsercreatens()](function.xml-parser-create-ns.html) - Створення XML-аналізатора з підтримкою просторів імен
-   [xmlparserfree()](function.xml-parser-free.html) - Звільнення XML-аналізатора
