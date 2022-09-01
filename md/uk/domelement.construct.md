---
navigation:
  - class.domelement.md: « DOMElement
  - domelement.getattribute.md: 'DOMElement::getAttribute »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::construct'
---
# DOMElement::construct

(PHP 5, PHP 7, PHP 8)

DOMElement::construct — Створює новий екземпляр класу DOMElement

### Опис

public **DOMElement::construct**(string `$qualifiedName`, ?string `$value` **`null`**, string `$namespace` = "")

Створює новий об'єкт класу [DOMElement](class.domelement.md). Цей об'єкт доступний лише для читання. Він може бути доданий до документа, але додаткові вузли до нього не можна додати, поки вузол не буде пов'язаний з документом. Щоб створити записуваний вузол, використовуйте [DOMDocument::createElement](domdocument.createelement.md) або [DOMDocument::createElementNS](domdocument.createelementns.md)

### Список параметрів

`qualifiedName`

Ім'я тега створюваного елемента. Якщо також передається параметр namespaceURI, ім'я елемента може приймати префікс, який має бути пов'язаний із URI.

`value`

Значення елемента.

`namespace`

URI простір імен для створення елемента з певним простіром імен.

### Приклади

**Приклад #1 Створення нового DOMElement**

```php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$element_ns = new DOMElement('pr:node1', 'thisvalue', 'http://xyz');
$element->appendChild($element_ns);
echo $dom->saveXML(); /* <?xml version="1.0" encoding="utf-8"?>
<root><pr:node1 xmlns:pr="http://xyz">thisvalue</pr:node1></root> */

?>
```

### Дивіться також

-   [DOMDocument::createElement()](domdocument.createelement.md) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) - Створити новий вузол елемента з відповідним простором імен
