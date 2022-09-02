---
navigation:
  - tidy.isxhtml.md: '« tidy::isXhtml'
  - tidy.parsefile.md: 'tidy::parseFile »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::isXml'
---
# tidy::isXml

# tidyісxml

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::isXml -- tidyісxml — Визначає, чи документ є спільним XML-документом (не HTML/XHTML)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::isXml(): bool
```

Процедурний стиль

```methodsynopsis
tidy_is_xml(tidy $tidy): bool
```

Визначає, чи документ є спільним XML-документом (не HTML/XHTML).

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Ця функція повертає \*\*`true`\*\*якщо зазначений tidy-об'єкт `tidy` є загальним XML-документом (не HTML/XHTML), або **`false`** в іншому випадку.

**Увага**

Ця функція ще не реалізована в самому Tidylib, тому завжди повертається **`false`**
