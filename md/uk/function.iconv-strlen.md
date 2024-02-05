---
navigation:
  - function.iconv-set-encoding.md: « iconv\_set\_encoding
  - function.iconv-strpos.md: iconv\_strpos »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: iconv\_strlen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iconv\_strlen

(PHP 5, PHP 7, PHP 8)

iconv\_strlen — Повертає кількість символів у рядку

### Опис

```methodsynopsis
iconv_strlen(string $string, ?string $encoding = null): int|false
```

В отличие от[strlen()](function.strlen.md) **iconv\_strlen()** враховує кодування рядка. Довжина `string` не обов'язково буде відповідати кількості байт у ній, так як у різних кодуваннях різні символи кодуються різною кількістю байт, наприклад, юнікод може бути і дво-, і чотирибайтним.

### Список параметрів

`string`

Рядок.

`encoding`

Якщо параметр `encoding` опущено, передбачається, що кодування рядка `string` еквівалентна значенню [iconv.internal\_encoding](iconv.configuration.md)

### Значення, що повертаються

Повертає кількість символів у `string` як ціле число або \*\*`false`\*\*в случае возникновения ошибки при кодировании.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `encoding` тепер допускає значення null. |

### Дивіться також

-   [grapheme\_strlen()](function.grapheme-strlen.md) \- отримує довжину рядка в одиницях графеми
-   [mb\_strlen()](function.mb-strlen.md) \- Отримує довжину рядка
-   [strlen()](function.strlen.md) \- Повертає довжину рядка
