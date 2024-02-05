---
navigation:
  - function.ps-end-pattern.md: « ps\_end\_pattern
  - function.ps-fill-stroke.md: ps\_fill\_stroke »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_end\_template
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_end\_template

(PECL ps >= 1.2.0)

ps\_end\_template — Завершує шаблон

### Опис

```methodsynopsis
ps_end_template(resource $psdoc): bool
```

Завершує шаблон, який було розпочато за допомогою [ps\_begin\_template()](function.ps-begin-template.md). Після завершення шаблону його можна використовувати як зображення.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_begin\_template()](function.ps-begin-template.md) \- Починає новий шаблон
