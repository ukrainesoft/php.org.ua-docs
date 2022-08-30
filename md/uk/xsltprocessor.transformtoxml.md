Перетворює на XML

-   [« XSLTProcessor::transformToUri](xsltprocessor.transformtouri.html)
    
-   [Модулі для роботи з GUI](refs.ui.html)
    
-   [PHP Manual](index.html)
    
-   [XSLTProcessor](class.xsltprocessor.html)
    
-   Перетворює на XML
    

# XSLTProcessor::transformToXml

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::transformToXml — Перетворює на XML

### Опис

```methodsynopsis
public XSLTProcessor::transformToXml(object $document): string|null|false
```

Перетворює вихідний вузол у рядок, застосовуючи таблиці стилів, які встановлені за допомогою методу [xsltprocessor::importStylesheet()](xsltprocessor.importstylesheet.html)

### Список параметрів

`document`

Об'єкт класу [DOMDocument](class.domdocument.html) або [SimpleXMLElement](class.simplexmlelement.html) для перетворення.

### Значення, що повертаються

Результат перетворення, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Трансформація у рядок**

```php
<?php

// Загрузка источника XML
$xml = new DOMDocument;
$xml->load('collection.xml');

$xsl = new DOMDocument;
$xsl->load('collection.xsl');

// Настройка преобразования
$proc = new XSLTProcessor;
$proc->importStyleSheet($xsl); // добавление стилей xsl

echo $proc->transformToXML($xml);

?>
```

Результат виконання цього прикладу:

```
Hey! Welcome to Nicolas Eliaszewicz's sweet CD collection!

<h1>Fight for your mind</h1><h2>by Ben Harper - 1995</h2><hr>
<h1>Electric Ladyland</h1><h2>by Jimi Hendrix - 1997</h2><hr>
```

### Дивіться також

-   [XSLTProcessor::transformToDoc()](xsltprocessor.transformtodoc.html) - Перетворює на DOMDocument
-   [XSLTProcessor::transformToUri()](xsltprocessor.transformtouri.html) - Перетворює на URI