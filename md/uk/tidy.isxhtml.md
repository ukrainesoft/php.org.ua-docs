---
navigation:
  - tidy.md.md: '« tidy::html'
  - tidy.isxml.md: 'tidy::isXml »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::isXhtml'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::isXhtml

# tidy\_is\_xhtml

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::isXhtml -- tidy\_is\_xhtml — Визначає, чи є документ XHTML-документом

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::isXhtml(): bool
```

Процедурний стиль

```methodsynopsis
tidy_is_xhtml(tidy $tidy): bool
```

Визначає, чи документ XHTML-документом.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Функція повертає \*\*`true`\*\*якщо зазначений tidy-об'єкт `tidy` є XHTML-документом, або **`false`** в іншому випадку.

**Увага**

Ця функція ще не реалізована в самому Tidylib, тому завжди повертається **`false`**
