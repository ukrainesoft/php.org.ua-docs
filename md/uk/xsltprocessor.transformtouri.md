---
navigation:
  - xsltprocessor.transformtodoc.md: '« XSLTProcessor::transformToDoc'
  - xsltprocessor.transformtoxml.md: 'XSLTProcessor::transformToXml »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::transformToUri'
---
# XSLTProcessor::transformToUri

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::transformToUri — Перетворює на URI

### Опис

```methodsynopsis
public XSLTProcessor::transformToURI(DOMDocument $doc, string $uri): int
```

Перетворює вихідний вузол URI, застосовуючи таблицю стилів, яка встановлена ​​за допомогою методу [XSLTProcessor::importStylesheet()](xsltprocessor.importstylesheet.md)

### Список параметрів

`doc`

Документ перетворення.

`uri`

Цільовий URI для перетворення.

### Значення, що повертаються

Повертає кількість записаних байтів, або **`false`** у разі виникнення помилки.

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

$proc->transformToURI($xml, 'file:///tmp/out.html');

?>
```

### Дивіться також

-   [XSLTProcessor::transformToDoc()](xsltprocessor.transformtodoc.md) - Перетворює на DOMDocument
-   [XSLTProcessor::transformToXml()](xsltprocessor.transformtoxml.md) - Перетворює на XML
