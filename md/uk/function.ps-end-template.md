---
navigation:
  - function.ps-end-pattern.md: «psendpattern
  - function.ps-fill-stroke.md: псfillstroke »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псendtemplate
---
# псendtemplate

(PECL ps >= 1.2.0)

псendtemplate — Завершує шаблон

### Опис

```methodsynopsis
ps_end_template(resource $psdoc): bool
```

Завершує шаблон, який було розпочато за допомогою [псbegintemplate()](function.ps-begin-template.md). Після завершення шаблону його можна використовувати як зображення.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псbegintemplate()](function.ps-begin-template.md) - Починає новий шаблон
