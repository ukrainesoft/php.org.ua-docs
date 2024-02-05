---
navigation:
  - function.imap-utf7-decode.md: « imap\_utf7\_decode
  - function.imap-utf8-to-mutf7.md: imap\_utf8\_to\_mutf7 »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_utf7\_encode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_utf7\_encode

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_utf7\_encode — Перетворює рядок у кодуванні ISO-8859-1 на модифіковане кодування UTF-7

### Опис

```methodsynopsis
imap_utf7_encode(string $string): string
```

Перетворює рядок `string` текст у модифікованому кодуванні UTF-7.

Це потрібно для кодування імен поштових скриньок, що містять у імені символи, що не входять до друкованого діапазону ASCII.

### Список параметрів

`string`

Рядок у кодуванні ISO-8859-1.

### Значення, що повертаються

Повертає рядок `string`, кодированную в модифицированную кодировку UTF-7 так, как определено в раздел 5.1.3 стандарта[» RFC 2060](http://www.faqs.org/rfcs/rfc2060)

### Дивіться також

-   [imap\_utf7\_decode()](function.imap-utf7-decode.md) \- Декодує рядок із модифікованого кодування UTF-7
