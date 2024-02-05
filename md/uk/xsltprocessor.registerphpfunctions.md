---
navigation:
  - xsltprocessor.importstylesheet.md: '« XSLTProcessor::importStylesheet'
  - xsltprocessor.removeparameter.md: 'XSLTProcessor::removeParameter »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::registerPHPFunctions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::registerPHPFunctions

(PHP 5 >= 5.0.4, PHP 7, PHP 8)

XSLTProcessor::registerPHPFunctions — Включає здатність функцій PHP працювати як функції XSLT

### Опис

```methodsynopsis
public XSLTProcessor::registerPHPFunctions(array|string|null $functions = null): void
```

Цей метод робить PHP функції доступними як XSLT-функції в таблицях стилів XSL.

### Список параметрів

`functions`

Використовуйте цей параметр, щоб дозволити виклик із XSLT лише окремих функцій.

Цей параметр може приймати або рядкове значення – назву функції, або масив – список назв.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Простий виклик функції PHP з таблиці стилів**

```php
<?php
$xml = <<<EOB
<allusers>
 <user>
  <uid>bob</uid>
 </user>
 <user>
  <uid>joe</uid>
 </user>
</allusers>
EOB;
$xsl = <<<EOB
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet version="1.0"
     xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
     xmlns:php="http://php.net/xsl">
<xsl:output method="html" encoding="utf-8" indent="yes"/>
 <xsl:template match="allusers">
  <html><body>
    <h2>Users</h2>
    <table>
    <xsl:for-each select="user">
      <tr><td>
        <xsl:value-of
             select="php:function('ucfirst',string(uid))"/>
      </td></tr>
    </xsl:for-each>
    </table>
  </body></html>
 </xsl:template>
</xsl:stylesheet>
EOB;
$xmldoc = new DOMDocument();
$xmldoc->loadXML($xml);
$xsldoc = new DOMDocument();
$xsldoc->loadXML($xsl);

$proc = new XSLTProcessor();
$proc->registerPHPFunctions();
$proc->importStyleSheet($xsldoc);
echo $proc->transformToXML($xmldoc);
?>
```
