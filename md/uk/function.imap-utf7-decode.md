---
navigation:
  - function.imap-unsubscribe.md: « imap\_unsubscribe
  - function.imap-utf7-encode.md: imap\_utf7\_encode »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_utf7\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_utf7\_decode

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_utf7\_decode — Декодує рядок із модифікованого кодування UTF-7

### Опис

```methodsynopsis
imap_utf7_decode(string $string): string|false
```

Декодирует`string` з модифікованого кодування UTF-7 ISO-8859-1.

Це потрібно для декодування імен поштових скриньок, що містять у імені символи, які не входять до друкованого діапазону ASCII.

### Список параметрів

`string`

Текст у модифікованому кодуванні UTF-7, як визначено в [» RFC 2060](http://www.faqs.org/rfcs/rfc2060), Розділ 5.1.3.

### Значення, що повертаються

Повертає рядок у кодуванні ISO-8859-1, який містить ту ж послідовність символів, що й `string`, или\*\*`false`\*\*, якщо `string` містить некоректні символи або якщо `string` містить символи, що не входять до набору символів ISO-8859-1.

### Дивіться також

-   [imap\_utf7\_encode()](function.imap-utf7-encode.md) \- Перетворює рядок у кодуванні ISO-8859-1 на модифіковане кодування UTF-7
