Створює новий об'єкт класу DOM Entity Reference

-   [« DOMEntityReference](class.domentityreference.html)
    
-   [DOMException »](class.domexception.html)
    
-   [PHP Manual](index.html)
    
-   [DOMEntityReference](class.domentityreference.html)
    
-   Створює новий об'єкт класу DOM Entity Reference
    

# DOMEntityReference::construct

(PHP 5, PHP 7, PHP 8)

DOMEntityReference::construct — Створює новий об'єкт класу DOM Entity Reference

### Опис

public **DOMEntityReference::construct**(string `$name`

Створює новий об'єкт класу [DOMEntityReference](class.domentityreference.html)

### Список параметрів

`name`

Ім'я посилання на суть.

### Приклади

**Приклад #1 Створення нового об'єкту DOMEntityReference**

```php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$entity = $element->appendChild(new DOMEntityReference('nbsp'));
echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root></root> */

?>
```

### Дивіться також

-   [DOMDocument::createEntityReference()](domdocument.createentityreference.html) - Створити новий вузол посилання на суть