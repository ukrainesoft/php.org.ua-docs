---
navigation:
  - class.domtext.md: « DOMText
  - domtext.iselementcontentwhitespace.md: 'DOMText::isElementContentWhitespace »'
  - index.md: PHP Manual
  - class.domtext.md: DOMText
title: 'DOMText::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMText::\_\_construct

(PHP 5, PHP 7, PHP 8)

DOMText::\_\_construct — Створює об'єкт класу [DOMText](class.domtext.md)

### Опис

public**DOMText::\_\_construct**(string`$data` = "")

Створює новий екземпляр класу [DOMText](class.domtext.md)

### Список параметрів

`data`

Значення текстового сайту. Якщо значення не передано, буде створено порожній текстовий вузол.

### Приклади

**Приклад #1 Створення нового сайту DOMText**

```php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$text = $element->appendChild(new DOMText('root value'));
echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root>root value</root> */

?>
```

### Дивіться також

-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
