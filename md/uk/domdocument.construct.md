---
navigation:
  - class.domdocument.md: « DOMDocument
  - domdocument.createattribute.md: 'DOMDocument::createAttribute »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::construct'
---
# DOMDocument::construct

(PHP 5, PHP 7, PHP 8)

DOMDocument::construct — Створює новий об'єкт DOMDocument

### Опис

public **DOMDocument::construct**(string `$version` = "1.0", string `$encoding` = "")

Створює новий об'єкт [DOMDocument](class.domdocument.md)

### Список параметрів

`version`

Номер версії документа як частина оголошення XML.

`encoding`

Кодування документа як частину об'яви XML.

### Приклади

**Приклад #1 Створення об'єкту DOMDocument**

```php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');

echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?> */

?>
```

### Дивіться також

-   [DOMImplementation::createDocument()](domimplementation.createdocument.md) - Створює об'єкт класу DOMDocument заданого типу з його елементом
