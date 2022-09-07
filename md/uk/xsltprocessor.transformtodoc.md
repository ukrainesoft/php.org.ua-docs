---
navigation:
  - xsltprocessor.setsecurityprefs.md: '« XSLTProcessor::setSecurityPrefs'
  - xsltprocessor.transformtouri.md: 'XSLTProcessor::transformToUri »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::transformToDoc'
---
# XSLTProcessor::transformToDoc

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::transformToDoc — Перетворює на DOMDocument

### Опис

```methodsynopsis
public XSLTProcessor::transformToDoc(object $document, ?string $returnClass = null): DOMDocument|false
```

Перетворює вихідний вузол на [DOMDocument](class.domdocument.md) застосовуючи таблицю стилів, задану за допомогою методу [XSLTProcessor::importStylesheet()](xsltprocessor.importstylesheet.md)

### Список параметрів

`document`

Вузол, який необхідно перетворити.

### Значення, що повертаються

Повертає [DOMDocument](class.domdocument.md) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перетворення на DOMDocument**

```php
<?php

// Загрузка исходного XML
$xml = new DOMDocument;
$xml->load('collection.xml');

$xsl = new DOMDocument;
$xsl->load('collection.xsl');

// Настройка преобразования
$proc = new XSLTProcessor;
$proc->importStyleSheet($xsl); // добавление стилей xsl

echo trim($proc->transformToDoc($xml)->firstChild->wholeText);

?>
```

Результат виконання цього прикладу:

```
Hey! Welcome to Nicolas Eliaszewicz's sweet CD collection!
```

### Дивіться також

-   [XSLTProcessor::transformToUri()](xsltprocessor.transformtouri.md) - Перетворює на URI
-   [XSLTProcessor::transformToXml()](xsltprocessor.transformtoxml.md) - Перетворює на XML
