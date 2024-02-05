---
navigation:
  - function.xml-set-character-data-handler.md: « xml\_set\_character\_data\_handler
  - function.xml-set-element-handler.md: xml\_set\_element\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_default\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_default\_handler

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_set\_default\_handler — Установка стандартного оброблювача.

### Опис

```methodsynopsis
xml_set_default_handler(XMLParser $parser, callable $handler): true
```

Задає стандартний обробник для XML-аналізатора `parser`

### Список параметрів

`parser`

Парсер XML.

`handler`

Якщо передається значення **`null`** або порожній рядок, обробник повертається в стан за замовчуванням.

Якщо параметр `handler` є типом [callable](language.types.callable.md), то як оброблювач встановлюється callable.

Якщо параметр `handler` є рядком (string), це може бути ім'я методу об'єкта, заданого за допомогою функції [xml\_set\_object()](function.xml-set-object.md)

Сигнатура оброблювача має бути:

```methodsynopsis
handler(XmlParser $parser, string $data): void
```

`parser`

XML-парсер, що викликає оброблювач.

`data`

Параметр`data` містить дані у вигляді текстового рядка. Це може бути оголошення XML, оголошення типу документа, сутності чи інші дані, котрим немає іншого оброблювача.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |
