---
navigation:
  - function.ps-end-pattern.html: «psendpattern
  - function.ps-fill-stroke.html: псfillstroke »
  - index.html: PHP Manual
  - ref.ps.html: Функції PS
title: псendtemplate
---
# псendtemplate

(PECL ps >= 1.2.0)

псendtemplate — Завершує шаблон

### Опис

```methodsynopsis
ps_end_template(resource $psdoc): bool
```

Завершує шаблон, який було розпочато за допомогою [псbegintemplate()](function.ps-begin-template.html). Після завершення шаблону його можна використовувати як зображення.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псbegintemplate()](function.ps-begin-template.html) - Починає новий шаблон
