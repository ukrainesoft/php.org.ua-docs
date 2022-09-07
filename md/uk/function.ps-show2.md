---
navigation:
  - function.ps-show-xy.md: «psshowзі
  - function.ps-show.md: псshow »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псshow2
---
# псshow2

(PECL ps >= 1.1.0)

псshow2 — Виводить текст у поточній позиції

### Опис

```methodsynopsis
ps_show2(resource $psdoc, string $text, int $len): bool
```

Виводить текст у поточній позиції. Не виводить більше `len` символів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`text`

Текст для виведення.

`len`

Максимальна кількість символів для виведення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
