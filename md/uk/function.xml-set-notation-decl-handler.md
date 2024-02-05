---
navigation:
  - function.xml-set-external-entity-ref-handler.md: « xml\_set\_external\_entity\_ref\_handler
  - function.xml-set-object.md: xml\_set\_object »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_notation\_decl\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_notation\_decl\_handler

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_set\_notation\_decl\_handler — Встановлення обробника оголошення умовних позначень

### Опис

```methodsynopsis
xml_set_notation_decl_handler(XMLParser $parser, callable $handler): true
```

Задає обробник оголошення позначень для XML-аналізатора `parser`

Розділ оголошення позначень є частиною DTD документа і має такий формат:

name systemId publicId?>

Смотрите[» розділ 4.7 специфікації XML 1.0](http://www.w3.org/TR/1998/REC-xml-19980210#Notations) для більш повного опису позначень (нотацій).

### Список параметрів

`parser`

Парсер XML.

`handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
handler(    XMLParser $parser,    string $notation_name,    string|false $base,    string $system_id,    string|false $public_id): void
```

`parser`

XML-парсер, що викликає оброблювач.

`notation_name`

Ім'я позначення у тому вигляді, як описано вище.

`base`

Це основа для дозволу системного ідентифікатора (`system_id`) Зовнішньої сутності.

`system_id`

Системний ідентифікатор оголошення зовнішнього позначення.

`public_id`

Загальнодоступний ідентифікатор об'яви зовнішнього позначення.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
