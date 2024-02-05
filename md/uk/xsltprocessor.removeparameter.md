---
navigation:
  - xsltprocessor.registerphpfunctions.md: '« XSLTProcessor::registerPHPFunctions'
  - xsltprocessor.setparameter.md: 'XSLTProcessor::setParameter »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::removeParameter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::removeParameter

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::removeParameter — Видалення параметра

### Опис

```methodsynopsis
public XSLTProcessor::removeParameter(string $namespace, string $name): bool
```

Видалення параметра, якщо його встановлено. Це дозволяє процесору використовувати значення таблиці стилів, встановлене за замовчуванням.

### Список параметрів

`namespace`

Простір імен URI для параметра XSLT.

`name`

Локальна назва XSLT параметра.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [XSLTProcessor::setParameter()](xsltprocessor.setparameter.md) \- Встановлює значення параметра
-   [XSLTProcessor::getParameter()](xsltprocessor.getparameter.md) \- Повертає значення параметра
