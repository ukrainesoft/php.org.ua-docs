---
navigation:
  - class.domcdatasection.html: « DOMCdataSection
  - class.domcharacterdata.html: DOMCharacterData »
  - index.html: PHP Manual
  - class.domcdatasection.html: DOMCdataSection
title: 'DOMCdataSection::construct'
---
# DOMCdataSection::construct

(PHP 5, PHP 7, PHP 8)

DOMCdataSection::construct — Створює новий екземпляр класу DOMCdataSection

### Опис

public **DOMCdataSection::construct**(string `$data`

Створює новий вузол CDATA. Працює як клас [DOMText](class.domtext.md)

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

-   [DOMText::construct()](domtext.construct.md) - Створює об'єкт класу DOMText
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) - Створити новий текстовий вузол
