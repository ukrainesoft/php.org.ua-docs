---
navigation:
  - class.domentityreference.md: « DOMEntityReference
  - class.domexception.md: DOMException »
  - index.md: PHP Manual
  - class.domentityreference.md: DOMEntityReference
title: 'DOMEntityReference::construct'
---
# DOMEntityReference::construct

(PHP 5, PHP 7, PHP 8)

DOMEntityReference::construct — Створює новий об'єкт класу DOM Entity Reference

### Опис

public **DOMEntityReference::construct**(string `$name`

Створює новий об'єкт класу [DOMEntityReference](class.domentityreference.md)

### Список параметрів

`name`

Ім'я посилання на суть.

### Приклади

**Приклад #1 Створення нового об'єкту DOMEntityReference**

```php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$entity = $element->appendChild(new DOMEntityReference('nbsp'));
echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root></root> */

?>
```

### Дивіться також

-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) - Створити новий вузол посилання на суть
