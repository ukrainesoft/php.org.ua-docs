---
navigation:
  - function.iconv-set-encoding.md: « iconvsetencoding
  - function.iconv-strpos.md: iconvstrpos »
  - index.md: PHP Manual
  - ref.iconv.md: Функции iconv
title: iconvstrlen
---
# iconvstrlen

(PHP 5, PHP 7, PHP 8)

iconvstrlen — Повертає кількість символів у рядку

### Опис

```methodsynopsis
iconv_strlen(string $string, ?string $encoding = null): int|false
```

На відміну від [strlen()](function.strlen.md) **iconvstrlen()** враховує кодування рядка. Довжина `string` не обов'язково буде відповідати кількості байт у ній, так як у різних кодуваннях різні символи кодуються різною кількістю байт, наприклад, юнікод може бути і дво-, і чотирибайтним.

### Список параметрів

`string`

Рядок.

`encoding`

Якщо параметр `encoding` опущено, передбачається, що кодування рядка `string` еквівалентна значенню [iconv.internalencoding](iconv.configuration.md)

### Значення, що повертаються

Повертає кількість символів у `string` як ціле число або **`false`** у разі виникнення помилки під час кодування.

### список змін

| Версия | Описание |
| --- | --- |
|  | `encoding` тепер допускає значення null. |

### Дивіться також

-   [graphemestrlen()](function.grapheme-strlen.md) - отримує довжину рядка в одиницях графеми
-   [мбstrlen()](function.mb-strlen.md) - Отримує довжину рядка
-   [strlen()](function.strlen.md) - Повертає довжину рядка
