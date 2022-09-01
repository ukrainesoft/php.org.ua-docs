---
navigation:
  - function.ps-delete.html: «psdelete
  - function.ps-end-pattern.html: псendpattern »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псendpage
---
# псendpage

(PECL ps >= 1.1.0)

псendpage — Завершує сторінку

### Опис

```methodsynopsis
ps_end_page(resource $psdoc): bool
```

Завершує сторінку, яку було розпочато за допомогою [псbeginpage()](function.ps-begin-page.html). Завершення сторінки призведе до виходу з поточного контексту малювання, який, наприклад, вимагає перезавантаження шрифтів, якщо вони завантажувалися на сторінці та налаштування багатьох інших параметрів малювання, таких як ширина лінії або колір.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псbeginpage()](function.ps-begin-page.html) - Починає нову сторінку
