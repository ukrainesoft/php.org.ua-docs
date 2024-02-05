---
navigation:
  - xsltprocessor.construct.md: '« XSLTProcessor::\_\_construct'
  - xsltprocessor.getsecurityprefs.md: 'XSLTProcessor::getSecurityPrefs »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::getParameter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::getParameter

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::getParameter — Повертає значення параметра

### Опис

```methodsynopsis
public XSLTProcessor::getParameter(string $namespace, string $name): string|false
```

Возвращает параметр, если он раньше установлен с помощью[XSLTProcessor::setParameter()](xsltprocessor.setparameter.md)

### Список параметрів

`namespace`

Простір імен URI для параметра XSLT.

`name`

Місцеве ім'я параметра XSLT.

### Значення, що повертаються

Значение параметра (в виде строки), или\*\*`false`\*\*якщо воно не встановлено.

### Дивіться також

-   [XSLTProcessor::setParameter()](xsltprocessor.setparameter.md) \- Встановлює значення параметра
-   [XSLTProcessor::removeParameter()](xsltprocessor.removeparameter.md) \- Видаляє параметр
