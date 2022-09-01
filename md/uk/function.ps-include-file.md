---
navigation:
  - function.ps-hyphenate.html: «pshyphenate
  - function.ps-lineto.html: псlineto »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псincludefile
---
# псincludefile

(PECL ps >= 1.3.4)

псincludefile — Читає зовнішній файл із необробленим кодом PostScript

### Опис

```methodsynopsis
ps_include_file(resource $psdoc, string $file): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`file`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
