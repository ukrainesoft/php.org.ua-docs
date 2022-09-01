---
navigation:
  - xsltprocessor.getsecurityprefs.html: '« XSLTProcessor::getSecurityPrefs'
  - xsltprocessor.importstylesheet.html: 'XSLTProcessor::importStylesheet »'
  - index.html: PHP Manual
  - class.xsltprocessor.html: XSLTProcessor
title: 'XSLTProcessor::hasExsltSupport'
---
# XSLTProcessor::hasExsltSupport

(PHP 5> = 5.0.4, PHP 7, PHP 8)

XSLTProcessor::hasExsltSupport — Визначає чи має PHP підтримку EXSLT

### Опис

```methodsynopsis
public XSLTProcessor::hasExsltSupport(): bool
```

Цей метод визначає чи був PHP налаштований з [» библиотекой EXSLT](http://xmlsoft.org/XSLT/EXSLT/index.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перевірка підтримки EXSLT**

```php
<?php

$proc = new XSLTProcessor;
if (!$proc->hasExsltSupport()) {
    die('EXSLT support not available');
}

// выполнение некоторых действий EXSLT ..

?>
```
