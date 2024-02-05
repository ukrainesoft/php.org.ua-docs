---
navigation:
  - class.xsltprocessor.md: « XSLTProcessor
  - xsltprocessor.getparameter.md: 'XSLTProcessor::getParameter »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::\_\_construct

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::\_\_construct — Створює новий екземпляр класу XSLTProcessor

### Опис

**XSLTProcessor::\_\_construct**()

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
