---
navigation:
  - function.mailparse-msg-parse-file.md: « mailparsemsgparsefile
  - function.mailparse-rfc822-parse-addresses.md: mailparserfc822parseaddresses »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsemsgparse
---
# mailparsemsgparse

(PECL mailparse >= 0.9.0)

mailparsemsgparse - Інкрементальне розбирає дані в буфер

### Опис

```methodsynopsis
mailparse_msg_parse(resource $mimemail, string $data): bool
```

Інкрементальне розбирає дані заданий MIME-ресурс.

Функція дозволяє обробляти файл частинами, замість читати і обробляти відразу весь масив даних.

### Список параметрів

`mimemail`

Коректний `MIME`ресурс.

`data`

> **Зауваження**
> 
> Повідомлення, що міститься в `filename`, має закінчуватися новим рядком (`CRLF`); інакше останній рядок повідомлення не буде проаналізовано.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
