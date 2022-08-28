Перетворює на DOMDocument

-   [« XSLTProcessor::setSecurityPrefs](xsltprocessor.setsecurityprefs.html)
    
-   [XSLTProcessor::transformToUri »](xsltprocessor.transformtouri.html)
    
-   [PHP Manual](index.html)
    
-   [XSLTProcessor](class.xsltprocessor.html)
    
-   Перетворює на DOMDocument
    

# XSLTProcessor::transformToDoc

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::transformToDoc — Перетворює на DOMDocument

### Опис

```methodsynopsis
public XSLTProcessor::transformToDoc(object $document, ?string $returnClass = null): DOMDocument|false
```

Перетворює вихідний вузол на [DOMDocument](class.domdocument.html) застосовуючи таблицю стилів, задану за допомогою методу [XSLTProcessor::importStylesheet()](xsltprocessor.importstylesheet.html)

### Список параметрів

`document`

Вузол, який необхідно перетворити.

### Значення, що повертаються

Повертає [DOMDocument](class.domdocument.html) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перетворення на DOMDocument**

```php
<?php

// Загрузка исходного XML
$xml = new DOMDocument;
$xml->load('collection.xml');

$xsl = new DOMDocument;
$xsl->load('collection.xsl');

// Настройка преобразования
$proc = new XSLTProcessor;
$proc->importStyleSheet($xsl); // добавление стилей xsl

echo trim($proc->transformToDoc($xml)->firstChild->wholeText);

?>
```

Результат виконання цього прикладу:

```
Hey! Welcome to Nicolas Eliaszewicz's sweet CD collection!
```

### Дивіться також

-   [XSLTProcessor::transformToUri()](xsltprocessor.transformtouri.html) - Перетворює на URI
-   [XSLTProcessor::transformToXml()](xsltprocessor.transformtoxml.html) - Перетворює на XML