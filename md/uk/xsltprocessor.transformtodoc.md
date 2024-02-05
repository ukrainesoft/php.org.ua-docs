---
navigation:
  - xsltprocessor.setsecurityprefs.md: '« XSLTProcessor::setSecurityPrefs'
  - xsltprocessor.transformtouri.md: 'XSLTProcessor::transformToUri »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::transformToDoc'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::transformToDoc

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::transformToDoc — Перетворює на документ

### Опис

```methodsynopsis
public XSLTProcessor::transformToDoc(object $document, ?string $returnClass = null): object|false
```

Перетворює вихідний вузол на документ (наприклад, на об'єкт [DOMDocument](class.domdocument.md)), застосовуючи таблицю стилів, задану методом [XSLTProcessor::importStylesheet()](xsltprocessor.importstylesheet.md)

### Список параметрів

`document`

Об'єкт класу [DOMDocument](class.domdocument.md), об'єкт класу [SimpleXMLElement](class.simplexmlelement.md) або libxml-сумісний об'єкт, який буде перетворено.

`returnClass`

Через цей необов'язковий параметр можна встановити клас об'єкта, який поверне **XSLTProcessor::transformToDoc()**. Цей клас повинен або розширювати, або бути об'єктом того ж класу, який передано в параметр `document`

### Значення, що повертаються

Возвращает результирующий документ или\*\*`false`\*\*в случае возникновения ошибки.

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

Результат виконання наведеного прикладу:

```
Hey! Welcome to Nicolas Eliaszewicz's sweet CD collection!
```

### Дивіться також

-   [XSLTProcessor::transformToUri()](xsltprocessor.transformtouri.md) \- Перетворює на URI
-   [XSLTProcessor::transformToXml()](xsltprocessor.transformtoxml.md) \- Перетворює на XML
