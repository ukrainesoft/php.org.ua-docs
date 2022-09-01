---
navigation:
  - function.ps-end-page.html: «psendpage
  - function.ps-end-template.html: псendtemplate »
  - index.html: PHP Manual
  - ref.ps.html: Функції PS
title: псendpattern
---
# псendpattern

(PECL ps >= 1.2.0)

псendpattern — Завершує шаблон

### Опис

```methodsynopsis
ps_end_pattern(resource $psdoc): bool
```

Завершує шаблон, який було розпочато з [псbeginpattern()](function.ps-begin-pattern.html). Коли шаблон закінчено, його можна використовувати як колір заливки областей.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псbeginpattern()](function.ps-begin-pattern.html) - Починає новий візерунок
