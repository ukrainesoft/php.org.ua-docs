- [« XSLTProcessor::importStylesheet](xsltprocessor.importstylesheet.md)
- [XSLTProcessor::removeParameter »](xsltprocessor.removeparameter.md)

- [PHP Manual](index.md)
- [XSLTProcessor](class.xsltprocessor.md)
- Включає можливість використовувати PHP функції як функції
XSLT

# XSLTProcessor::registerPHPFunctions

(PHP 5 \>= 5.0.4, PHP 7, PHP 8)

XSLTProcessor::registerPHPFunctions — Включає можливість використання
PHP функції як функції XSLT

### Опис

public **XSLTProcessor::registerPHPFunctions**(array\|string\|null
`$functions` = **`null`**): void

Цей метод дозволяє використовувати PHP функції як функції XSLT в XSL
таблиці стилів.

### Список параметрів

`functions`
Використовуйте цей параметр, якщо хочете викликати з XSLT лише деякі
функції із.

Цей параметр може набувати або рядкове значення - назва
функції, чи масив - перелік назв.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Простий виклик функції PHP з таблиці стилів**

` <?php$xml = <<<<EOB<allusers> <user> <uid>bob</uid> </user> <user>  <uid>joe</uid> </user></allusers>EOB; $xsl==<<<<EOB<?xml version="1.0" encoding="UTF-8"?><xsl:stylesheet version="1.0"    xmlns:xsl="http://www.w3.org/1999/ XSL/Transform"    xmlns:php="http://php.net/xsl"><xsl:output method="html" encoding="utf-8" indent="yes"/> <xsl:template match=" allusers">  <html><body>    <h2>Users</h2>    <table>    <xsl:for-each select="user">      <tr><td>        <xsl:value-of             select="php:function ('ucfirst',string(uid))"/>      </td></tr>    </xsl:for-each>    </table>  </body></html> </xsl:template></xsl :stylesheet>EOB;$xmldoc= DOMDocument::loadXML($xml);$xsldoc = DOMDocument::loadXML($xsl);$proc = newXSLTProcessor();$proc->registerPHPFunctions();$ ($xsldoc);echo $proc->transformToXML($xmldoc);?> `
