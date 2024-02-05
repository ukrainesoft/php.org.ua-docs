---
navigation:
  - function.ps-show-xy.md: « ps\_show\_xy
  - function.ps-show.md: ps\_show »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_show2
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_show2

(PECL ps >= 1.1.0)

ps\_show2 — Виводить текст у поточній позиції

### Опис

```methodsynopsis
ps_show2(resource $psdoc, string $text, int $len): bool
```

Виводить текст у поточній позиції. Не виводить більше `len` символів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`text`

Текст для виведення.

`len`

Максимальна кількість символів для виведення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
