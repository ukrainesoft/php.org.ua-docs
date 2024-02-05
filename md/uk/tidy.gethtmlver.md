---
navigation:
  - tidy.getconfig.md: '« tidy::getConfig'
  - tidy.getopt.md: 'tidy::getOpt »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::getHtmlVer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::getHtmlVer

# tidy\_get\_html\_ver

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::getHtmlVer -- tidy\_get\_html\_ver — Отримує виявлену HTML версію для зазначеного документа

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::getHtmlVer(): int
```

Процедурний стиль

```methodsynopsis
tidy_get_html_ver(tidy $tidy): int
```

Повертає виявлену HTML версію для вказаного об'єкту tidy `tidy`

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає виявлену HTML-версію.

**Увага**

Функція ще не реалізована в самому Tidylib, тому завжди повертається
