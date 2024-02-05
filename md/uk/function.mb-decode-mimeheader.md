---
navigation:
  - function.mb-convert-variables.md: « mb\_convert\_variables
  - function.mb-decode-numericentity.md: mb\_decode\_numericentity »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_decode\_mimeheader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_decode\_mimeheader

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_decode\_mimeheader — Декодує рядок у MIME-заголовку

### Опис

```methodsynopsis
mb_decode_mimeheader(string $string): string
```

Декодує в MIME-заголовку передану параметр `string` закодований рядок (string).

### Список параметрів

`string`

Рядок (string) для декодування.

### Значення, що повертаються

Повертає декодований рядок (string) у внутрішньому кодуванні скрипта.

### Дивіться також

-   [mb\_encode\_mimeheader()](function.mb-encode-mimeheader.md) \- Кодує рядок для MIME-заголовка
