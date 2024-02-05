---
navigation:
  - function.xml-set-element-handler.md: « xml\_set\_element\_handler
  - function.xml-set-external-entity-ref-handler.md: xml\_set\_external\_entity\_ref\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_end\_namespace\_decl\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_end\_namespace\_decl\_handler

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

xml\_set\_end\_namespace\_decl\_handler — Встановлення обробника виходу за межі простору імен

### Опис

```methodsynopsis
xml_set_end_namespace_decl_handler(XMLParser $parser, callable $handler): true
```

Задає обробник, який викликається під час виходу межі оголошення простору імен. Цей обробник буде викликатись для кожного оголошення простору імен після того, як обробляє закінчення елемента, в якому цей простір імен було оголошено.

**Застереження**

Ця подія не підтримується LibXML, тому зареєстрований обробник не буде називатися.

### Список параметрів

`parser`

Парсер XML.

`handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
handler(XMLParser $parser, string|false $prefix)
```

`parser`

XML-парсер, що викликає оброблювач.

`prefix`

Префікс - рядок, що використовується як посилання на простір імен у межах об'єкта XML . \*\*`false`\*\*якщо префікс не існує.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |

### Дивіться також

-   [xml\_set\_start\_namespace\_decl\_handler()](function.xml-set-start-namespace-decl-handler.md) \- Встановлює обробник входу у межі простору імен
