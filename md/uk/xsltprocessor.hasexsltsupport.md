---
navigation:
  - xsltprocessor.getsecurityprefs.md: '« XSLTProcessor::getSecurityPrefs'
  - xsltprocessor.importstylesheet.md: 'XSLTProcessor::importStylesheet »'
  - index.md: PHP Manual
  - class.xsltprocessor.md: XSLTProcessor
title: 'XSLTProcessor::hasExsltSupport'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XSLTProcessor::hasExsltSupport

(PHP 5 >= 5.0.4, PHP 7, PHP 8)

XSLTProcessor::hasExsltSupport — Визначає чи має PHP підтримку EXSLT

### Опис

```methodsynopsis
public XSLTProcessor::hasExsltSupport(): bool
```

Цей метод визначає чи був PHP налаштований з [»Бібліотекою EXSLT](http://xmlsoft.org/XSLT/EXSLT/index.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Перевірка підтримки EXSLT**

```php
<?php

$proc = new XSLTProcessor;
if (!$proc->hasExsltSupport()) {
    die('EXSLT support not available');
}

// выполнение некоторых действий EXSLT ..

?>
```
