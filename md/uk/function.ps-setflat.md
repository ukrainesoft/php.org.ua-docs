---
navigation:
  - function.ps-setdash.md: « ps\_setdash
  - function.ps-setfont.md: ps\_setfont »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setflat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setflat

(PECL ps >= 1.1.0)

ps\_setflat - Встановлює площинність

### Опис

```methodsynopsis
ps_setflat(resource $psdoc, float $value): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`value`

`value` має бути між 0.2 та 1.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
