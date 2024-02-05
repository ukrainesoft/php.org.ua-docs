---
navigation:
  - function.ps-end-page.md: « ps\_end\_page
  - function.ps-end-template.md: ps\_end\_template »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_end\_pattern
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_end\_pattern

(PECL ps >= 1.2.0)

ps\_end\_pattern — Завершує шаблон

### Опис

```methodsynopsis
ps_end_pattern(resource $psdoc): bool
```

Завершує шаблон, який було розпочато з [ps\_begin\_pattern()](function.ps-begin-pattern.md). Коли шаблон закінчено, його можна використовувати як колір заливки областей.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_begin\_pattern()](function.ps-begin-pattern.md) \- Починає новий візерунок
