---
navigation:
  - class.xsltprocessor.md: « XSLTProcessor
  - xsltprocessor.getparameter.md: 'XSLTProcessor::getParameter »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::construct'
---
# XSLTProcessor::construct

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::construct — Створює новий екземпляр класу XSLTProcessor

### Опис

**XSLTProcessor::construct**

Створює новий екземпляр класу [XSLTProcessor](class.xsltprocessor.md)

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Створює [XSLTProcessor](class.xsltprocessor.md)**

```php
<?php

$xsldoc = new DOMDocument();
$xsldoc->load($xsl_filename);

$xmldoc = new DOMDocument();
$xmldoc->load($xml_filename);

$xsl = new XSLTProcessor();
$xsl->importStyleSheet($xsldoc);
echo $xsl->transformToXML($xmldoc);

?>
```
