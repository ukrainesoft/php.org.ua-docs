---
navigation:
  - function.mb-convert-variables.md: « mbconvertvariables
  - function.mb-decode-numericentity.md: мбdecodenumericentity »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбdecodemimeheader
---
# мбdecodemimeheader

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбdecodemimeheader — Декодує рядок у MIME-заголовку

### Опис

```methodsynopsis
mb_decode_mimeheader(string $string): string
```

Декодує закодований рядок (string) `string` у MIME-заголовку.

### Список параметрів

`string`

Рядок (string) для декодування.

### Значення, що повертаються

Декодований рядок (string) у внутрішньому кодуванні скрипта.

### Дивіться також

-   [мбencodemimeheader()](function.mb-encode-mimeheader.md) - Кодує рядок для MIME-заголовка
