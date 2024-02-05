---
navigation:
  - function.ps-delete.md: « ps\_delete
  - function.ps-end-pattern.md: ps\_end\_pattern »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_end\_page
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_end\_page

(PECL ps >= 1.1.0)

ps\_end\_page — Завершує сторінку

### Опис

```methodsynopsis
ps_end_page(resource $psdoc): bool
```

Завершує сторінку, яку було розпочато за допомогою [ps\_begin\_page()](function.ps-begin-page.md). Завершення сторінки призведе до виходу з поточного контексту малювання, який, наприклад, вимагає перезавантаження шрифтів, якщо вони завантажувалися на сторінці та налаштування багатьох інших параметрів малювання, таких як ширина лінії або колір.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_begin\_page()](function.ps-begin-page.md) \- Починає нову сторінку
