---
navigation:
  - tidy.getconfig.html: '« tidy::getConfig'
  - tidy.getopt.html: 'tidy::getOpt »'
  - index.html: PHP Manual
  - class.tidy.html: tidy
title: 'tidy::getHtmlVer'
---
# tidy::getHtmlVer

# tidygethtmlver

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::getHtmlVer -- tidygethtmlver — Отримує виявлену HTML версію для зазначеного документа

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

Повертає виявлену версію HTML.

**Увага**

Функція ще не реалізована в самому Tidylib, тому завжди повертається `0`
