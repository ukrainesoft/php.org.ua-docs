---
navigation:
  - xsltprocessor.removeparameter.html: '« XSLTProcessor::removeParameter'
  - xsltprocessor.setprofiling.html: 'XSLTProcessor::setProfiling »'
  - index.html: PHP Manual
  - class.xsltprocessor.html: XSLTProcessor
title: 'XSLTProcessor::setParameter'
---
# XSLTProcessor::setParameter

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::setParameter — Встановлює значення параметра

### Опис

```methodsynopsis
public XSLTProcessor::setParameter(string $namespace, string $name, string $value): bool
```

```methodsynopsis
public XSLTProcessor::setParameter(string $namespace, array $options): bool
```

Встановлює значення для одного або кількох параметрів, щоб використовувати надалі у перетвореннях [XSLTProcessor](class.xsltprocessor.html). Якщо параметра немає в таблиці стилів, він буде проігнорований.

### Список параметрів

`namespace`

Простір імен URI для параметра XSLT.

`name`

Локальна назва параметра XSLT.

`value`

Нове значення параметра XSLT.

`options`

Масив пар `name => value`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Зміна власника перед перетворенням**

```php
<?php

$collections = array(
    'Marc Rutkowski' => 'marc',
    'Olivier Parmentier' => 'olivier'
);

$xsl = new DOMDocument;
$xsl->load('collection.xsl');

// Настройка преобразования
$proc = new XSLTProcessor;
$proc->importStyleSheet($xsl); // добавление стилей xsl

foreach ($collections as $name => $file) {
    // Load the XML source
    $xml = new DOMDocument;
    $xml->load('collection_' . $file . '.xml');

    $proc->setParameter('', 'owner', $name);
    $proc->transformToURI($xml, 'file:///tmp/' . $file . '.html');
}

?>
```

### Дивіться також

-   [XSLTProcessor::getParameter()](xsltprocessor.getparameter.html) - Повертає значення параметра
-   [XSLTProcessor::removeParameter()](xsltprocessor.removeparameter.html) - Видаляє параметр
