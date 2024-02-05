---
navigation:
  - function.xml-set-processing-instruction-handler.md: « xml\_set\_processing\_instruction\_handler
  - function.xml-set-unparsed-entity-decl-handler.md: xml\_set\_unparsed\_entity\_decl\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_start\_namespace\_decl\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_start\_namespace\_decl\_handler

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

xml\_set\_start\_namespace\_decl\_handler - Встановлює обробник входу в межі простору імен

### Опис

```methodsynopsis
xml_set_start_namespace_decl_handler(XMLParser $parser, callable $handler): true
```

Задає обробник події входу до простору імен. Тобто обробник викликається аналізатор знаходить оголошення простору імен. Подібні оголошення знаходяться у елементах, що відкривають тегах. Цей оброблювач викликається до оброблювача початку тега.

### Список параметрів

`parser`

Парсер XML.

`handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура обробника має бути такою:

```methodsynopsis
handler(XMLParser $parser, string|false $prefix, string $uri): void
```

`parser`

XML-парсер, що викликає оброблювач.

`prefix`

Префікс — рядок-посилання на простір імен у межах об'єкта XML. Логічне значення \*\*`false`\*\*якщо префікс не існує.

`uri`

Універсальний ідентифікатор ресурсу (URI) простір імен.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |

### Дивіться також

-   [xml\_set\_end\_namespace\_decl\_handler()](function.xml-set-end-namespace-decl-handler.md) \- встановлення обробника виходу за межі простору імен
