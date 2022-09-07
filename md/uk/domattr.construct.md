---
navigation:
  - class.domattr.md: « DOMAttr
  - domattr.isid.md: 'DOMAttr::isId »'
  - index.md: PHP Manual
  - class.domattr.md: DOMAttr
title: 'DOMAttr::construct'
---
# DOMAttr::construct

(PHP 5, PHP 7, PHP 8)

DOMAttr::construct - Створює екземпляр класу [DOMAttr](class.domattr.md)

### Опис

public **DOMAttr::construct**(string `$name`, string `$value` = "")

Створює новий об'єкт класу DOMAttr. Цей об'єкт буде доступний лише для читання. Він може бути доданий до документа, але додаткові вузли не можна додати до цього вузла, доки він приєднаний до документа. Для створення вузла з можливістю модифікації використовуйте [DOMDocument::createAttribute](domdocument.createattribute.md)

### Список параметрів

`name`

Ім'я тег атрибут.

`value`

Значення атрибуту.

### Приклади

**Приклад #1 Створення нового об'єкта класу [DOMAttr](class.domattr.md)**

```php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$attr = $element->setAttributeNode(new DOMAttr('attr', 'attrvalue'));
echo $dom->saveXML();

?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<root attr="attrvalue" />
```

### Дивіться також

-   [DOMDocument::createAttribute()](domdocument.createattribute.md) - Створити новий атрибут
