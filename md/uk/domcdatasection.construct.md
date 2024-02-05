---
navigation:
  - class.domcdatasection.md: « DOMCdataSection
  - class.domcharacterdata.md: DOMCharacterData »
  - index.md: PHP Manual
  - class.domcdatasection.md: DOMCdataSection
title: 'DOMCdataSection::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCdataSection::\_\_construct

(PHP 5, PHP 7, PHP 8)

DOMCdataSection::\_\_construct — Створює новий екземпляр класу DOMCdataSection

### Опис

public**DOMCdataSection::\_\_construct**(string`$data`) .

Створює новий вузол CDATA. Працює як клас [DOMText](class.domtext.md)

### Список параметрів

`data`

Значення вузла CDATA. Якщо не вказано, створюється порожній вузол CDATA.

### Приклади

**Приклад #1 Створення об'єкта класу DOMCdataSection**

```php
<?php

$dom = new DOMDocument('1.0', 'utf-8');
$element = $dom->appendChild(new DOMElement('root'));
$text = $element->appendChild(new DOMCdataSection('root value'));
echo $dom->saveXML();

?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<root><![CDATA[root value]]></root>
```

### Дивіться також

-   [DOMText::\_\_construct()](domtext.construct.md) \- Створює об'єкт класу DOMText
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
