---
navigation:
  - xsl.examples-collection.md: « Файли collection.xml та collection.xsl для прикладів
  - class.xsltprocessor.md: XSLTProcessor »
  - index.md: PHP Manual
  - xsl.examples.md: Приклади
title: Обробка помилок за допомогою функцій обробки помилок libxml
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Обробка помилок за допомогою функцій обробки помилок libxml

libxml надає ряд функцій для обробки помилок, які можуть використовуватися для вилову та роботи з помилками під час обробки XSLT.

**Приклад #1 fruits.xml**

Правильний XML.

Apple Banana Cherry

**Приклад #2 fruits.xsl**

Містить неправильне "select" вираз.

<xsl:stylesheet version="1.0" xmlns:xsl="[http://www.w3.org/1999/XSL/Transform">](http://www.w3.org/1999/XSL/Transform%22%3E) <xsl:output method="html" encoding="utf-8" indent="no"/> <xsl:template match="fruits">

[xsl:apply-templates/](xsl:apply-templates/)

<xsl:template match="fruit">- <xsl:value-of select="THIS IS A DELIBERATE ERROR!"/>

**Приклад #3 Збір та виведення помилок**

Приклад нижче відловлює та відображає помилки libxml, що з'являються під час виклику методу [XSLTProcessor::importStyleSheet()](xsltprocessor.importstylesheet.md) зі стилем, що містить помилки.

```php
<?php

$xmldoc = new DOMDocument();
$xsldoc = new DOMDocument();
$xsl = new XSLTProcessor();

$xmldoc->loadXML('fruits.xml');
$xsldoc->loadXML('fruits.xsl');

libxml_use_internal_errors(true);
$result = $xsl->importStyleSheet($xsldoc);
if (!$result) {
    foreach (libxml_get_errors() as $error) {
        echo "Libxml error: {$error->message}\n";
    }
}
libxml_use_internal_errors(false);

if ($result) {
    echo $xsl->transformToXML($xmldoc);
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
Libxml error: Invalid expression

Libxml error: compilation error: file fruits.xsl line 9 element value-of
Libxml error: xsl:value-of : could not compile select expression 'THIS IS A DELIBERATE ERROR!'
```
