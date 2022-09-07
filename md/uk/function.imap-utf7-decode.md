---
navigation:
  - function.imap-unsubscribe.md: « imapunsubscribe
  - function.imap-utf7-encode.md: imaputf7encode »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imaputf7decode
---
# imaputf7decode

(PHP 4, PHP 5, PHP 7, PHP 8)

imaputf7decode — Декодує рядок із модифікованого кодування UTF-7

### Опис

```methodsynopsis
imap_utf7_decode(string $string): string|false
```

Декодує `string` з модифікованого кодування UTF-7 ISO-8859-1.

Це потрібно для декодування імен поштових скриньок, що містять у імені символи, які не входять до друкованого діапазону ASCII.

### Список параметрів

`string`

Текст у модифікованому кодуванні UTF-7, як визначено в [» RFC 2060](http://www.faqs.org/rfcs/rfc2060), Розділ 5.1.3.

### Значення, що повертаються

Повертає рядок у кодуванні ISO-8859-1, який містить ту ж послідовність символів, що й `string`, або **`false`**, якщо `string` містить некоректні символи або якщо `string` містить символи, що не входять до набору символів ISO-8859-1.

### Дивіться також

-   [imaputf7encode()](function.imap-utf7-encode.md) - Перетворює рядок ISO-8859-1 на модифікований UTF-7
