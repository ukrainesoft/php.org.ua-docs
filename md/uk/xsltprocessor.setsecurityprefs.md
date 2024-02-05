---
navigation:
  - xsltprocessor.setprofiling.md: '« XSLTProcessor::setProfiling'
  - xsltprocessor.transformtodoc.md: 'XSLTProcessor::transformToDoc »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::setSecurityPrefs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::setSecurityPrefs

(PHP >= 5.4.0, PHP 7, PHP 8)

XSLTProcessor::setSecurityPrefs — Встановити налаштування безпеки

### Опис

```methodsynopsis
public XSLTProcessor::setSecurityPrefs(int $preferences): int
```

Встановлює налаштування безпеки.

### Список параметрів

`preferences`

Нові параметри безпеки. Бітова маска з: **`XSL_SECPREF_READ_FILE`** **`XSL_SECPREF_WRITE_FILE`** **`XSL_SECPREF_CREATE_DIRECTORY`** **`XSL_SECPREF_READ_NETWORK`** **`XSL_SECPREF_WRITE_NETWORK`**. Або, альтернативно, можна передати **`XSL_SECPREF_NONE`** або **`XSL_SECPREF_DEFAULT`**

### Значення, що повертаються

Повертає старі параметри безпеки.
