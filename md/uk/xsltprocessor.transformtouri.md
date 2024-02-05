---
navigation:
  - xsltprocessor.transformtodoc.md: '« XSLTProcessor::transformToDoc'
  - xsltprocessor.transformtoxml.md: 'XSLTProcessor::transformToXml »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::transformToUri'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::transformToUri

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::transformToUri — Перетворює на URI

### Опис

```methodsynopsis
public XSLTProcessor::transformToUri(object $document, string $uri): int
```

Перетворює вихідний вузол URI, застосовуючи таблицю стилів, яка встановлена ​​методом [XSLTProcessor::importStylesheet()](xsltprocessor.importstylesheet.md)

### Список параметрів

`document`

Перетворюваний об'єкт [DOMDocument](class.domdocument.md) або [SimpleXMLElement](class.simplexmlelement.md)

`uri`

Цільовий URI для перетворення.

### Значення, що повертаються

Повертає кількість записаних байтів, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Перетворення на HTML файл**

```php
<?php

// Загрузка источника XML
$xml = new DOMDocument;
$xml->load('collection.xml');

$xsl = new DOMDocument;
$xsl->load('collection.xsl');

// Настройка преобразования
$proc = new XSLTProcessor;
$proc->importStyleSheet($xsl); // добавление стилей xsl

$proc->transformToURI($xml, 'file:///tmp/out.md');

?>
```

### Дивіться також

-   [XSLTProcessor::transformToDoc()](xsltprocessor.transformtodoc.md) \- Перетворює на документ
-   [XSLTProcessor::transformToXml()](xsltprocessor.transformtoxml.md) \- Перетворює на XML
