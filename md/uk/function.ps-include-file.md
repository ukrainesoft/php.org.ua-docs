---
navigation:
  - function.ps-hyphenate.md: « ps\_hyphenate
  - function.ps-lineto.md: ps\_lineto »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_include\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_include\_file

(PECL ps >= 1.3.4)

ps\_include\_file — Читає зовнішній файл із необробленим кодом PostScript

### Опис

```methodsynopsis
ps_include_file(resource $psdoc, string $file): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`file`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
