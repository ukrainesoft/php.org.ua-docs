---
navigation:
  - function.xml-set-default-handler.md: « xml\_set\_default\_handler
  - function.xml-set-end-namespace-decl-handler.md: xml\_set\_end\_namespace\_decl\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_element\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_element\_handler

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_set\_element\_handler — Встановлення обробника початкового та кінцевого елементів

### Опис

```methodsynopsis
xml_set_element_handler(XMLParser $parser, callable $start_handler, callable $end_handler): true
```

Встановлює функцію обробник елементів для XML-аналізатора `parser`

Параметр`start_handler` викликається при відкритті нового XML-елемента. Параметр `end_handler` викликається під час закриття XML-елемента.

### Список параметрів

`parser`

Парсер XML.

`start_handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
start_element_handler(XMLParser $parser, string $name, array $attributes): void
```

`parser`

XML-парсер, що викликає оброблювач.

`name`

Містить ім'я елемента, якого викликається даний обробник. Якщо для цього синтаксичного аналізатора діє [приведення до одного регістру](xml.case-folding.md), то ім'я елемента буде у верхньому регістрі.

`attributes`

Асоціативний масив із атрибутами елемента. Масив порожній, якщо елемент не має атрибутів. Ключами цього масиву є імена атрибутів, значення - значення атрибутів. Імена атрибутів [наводяться до одного регістру](xml.case-folding.md) за тими ж критеріями, як і імена елементів. Значення атрибутів *не* наводяться до одного регістру. Порядок отримання атрибутів `attributes` ідентичний порядку оголошення атрибутів.

`end_element`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
end_element_handler(resource $parser, string $name): void
```

`parser`

XML-парсер, що викликає оброблювач.

`name`

Містить ім'я елемента, якого викликається даний обробник. Якщо для цього синтаксичного аналізатора діє [приведення до одного регістру](xml.case-folding.md), то ім'я елемента буде у верхньому регістрі.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
