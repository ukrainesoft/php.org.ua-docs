Створює новий екземпляр класу DOMCdataSection

-   [« DOMCdataSection](class.domcdatasection.html)
    
-   [DOMCharacterData »](class.domcharacterdata.html)
    
-   [PHP Manual](index.html)
    
-   [DOMCdataSection](class.domcdatasection.html)
    
-   Створює новий екземпляр класу DOMCdataSection
    

# DOMCdataSection::construct

(PHP 5, PHP 7, PHP 8)

DOMCdataSection::construct — Створює новий екземпляр класу DOMCdataSection

### Опис

public **DOMCdataSection::construct**(string `$data`

Створює новий вузол CDATA. Працює як клас [DOMText](class.domtext.html)

### Список параметрів

`data`

Значення вузла CDATA. Якщо не вказано, створюється пустий вузол CDATA.

### Приклади

**Приклад #1 Створення об'єкта класу DOMCdataSection**

```php
<?php

$dom = new DOMDocument('1.0', 'utf-8');
$element = $dom->appendChild(new DOMElement('root'));
$text = $element->appendChild(new DOMCdataSection('root value'));
echo $dom->saveXML();

?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<root><![CDATA[root value]]></root>
```

### Дивіться також

-   [DOMText::\_\_construct()](domtext.construct.html) - Створює об'єкт класу DOMText
-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол