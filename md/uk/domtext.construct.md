Створює об'єкт класу DOMText

-   [« DOMText](class.domtext.html)
    
-   [DOMText::isElementContentWhitespace »](domtext.iselementcontentwhitespace.html)
    
-   [PHP Manual](index.html)
    
-   [DOMText](class.domtext.html)
    
-   Створює об'єкт класу DOMText
    

# DOMText::construct

(PHP 5, PHP 7, PHP 8)

DOMText::construct — Створює об'єкт класу [DOMText](class.domtext.html)

### Опис

public **DOMText::construct**(string `$data` = "")

Створює новий екземпляр класу [DOMText](class.domtext.html)

### Список параметрів

`data`

Значення текстового сайту. Якщо значення не передано, буде створено порожній текстовий вузол.

### Приклади

**Приклад #1 Створення нового сайту DOMText**

```php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$text = $element->appendChild(new DOMText('root value'));
echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root>root value</root> */

?>
```

### Дивіться також

-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол