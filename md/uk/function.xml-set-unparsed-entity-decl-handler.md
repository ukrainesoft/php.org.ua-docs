---
navigation:
  - function.xml-set-start-namespace-decl-handler.md: « xml\_set\_start\_namespace\_decl\_handler
  - class.xmlparser.md: XmlParser »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_unparsed\_entity\_decl\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_unparsed\_entity\_decl\_handler

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_set\_unparsed\_entity\_decl\_handler — Встановлення оброблювача нерозібраних оголошень сутностей

### Опис

```methodsynopsis
xml_set_unparsed_entity_decl_handler(XMLParser $parser, callable $handler): true
```

Задає функцію обробник нерозібраних оголошень для XML-аналізатора `parser`

Обработчик`handler` буде викликано, якщо XML-аналізатор виявить NDATA-оголошення зовнішньої сутності вигляду:

name publicId systemId} NDATAnotationName

Смотрите[» розділ 4.2.2 XML 1.0 специфікації](http://www.w3.org/TR/1998/REC-xml-19980210#sec-external-ent)щоб отримати точне визначення позначень зовнішніх сутностей.

### Список параметрів

`parser`

Парсер XML.

`handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
handler(    XMLParser $parser,    string $entity_name,    string|false $base,    string $system_id,    string|false $public_id,    string|false $notation_name): void
```

`parser`

XML-парсер, що викликає оброблювач.

`entity_name`

Ім'я сутності, яку потрібно дати визначення.

`base`

Це основа для дозволу системного ідентифікатора (`system_id`) Зовнішньої сутності.

`system_id`

Системний ідентифікатор зовнішньої сутності

`public_id`

Загальнодоступний ідентифікатор зовнішньої сутності.

`notation_name`

Ім'я позначення цієї сутності (дивіться [xml\_set\_notation\_decl\_handler()](function.xml-set-notation-decl-handler.md)

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
