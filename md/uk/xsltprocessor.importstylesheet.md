---
navigation:
  - xsltprocessor.hasexsltsupport.md: '« XSLTProcessor::hasExsltSupport'
  - xsltprocessor.registerphpfunctions.md: 'XSLTProcessor::registerPHPFunctions »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::importStylesheet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::importStylesheet

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::importStylesheet — Імпортує таблицю стилів

### Опис

```methodsynopsis
public XSLTProcessor::importStylesheet(object $stylesheet): bool
```

Цей метод імпортує таблицю стилів у [XSLTProcessor](class.xsltprocessor.md) для трансформації.

### Список параметрів

`stylesheet`

Імпортована таблиця стилів у вигляді об'єкта [DOMDocument](class.domdocument.md) або [SimpleXMLElement](class.simplexmlelement.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
