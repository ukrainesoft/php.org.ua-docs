---
navigation:
  - xsltprocessor.getparameter.md: '« XSLTProcessor::getParameter'
  - xsltprocessor.hasexsltsupport.md: 'XSLTProcessor::hasExsltSupport »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::getSecurityPrefs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::getSecurityPrefs

(PHP >= 5.4.0, PHP 7, PHP 8)

XSLTProcessor::getSecurityPrefs — Отримати налаштування безпеки

### Опис

```methodsynopsis
public XSLTProcessor::getSecurityPrefs(): int
```

Отримує налаштування безпеки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Бітова маска, що складається з **`XSL_SECPREF_READ_FILE`** **`XSL_SECPREF_WRITE_FILE`** **`XSL_SECPREF_CREATE_DIRECTORY`** **`XSL_SECPREF_READ_NETWORK`** **`XSL_SECPREF_WRITE_NETWORK`**
