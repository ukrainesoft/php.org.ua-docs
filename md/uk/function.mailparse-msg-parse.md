---
navigation:
  - function.mailparse-msg-parse-file.md: « mailparse\_msg\_parse\_file
  - function.mailparse-rfc822-parse-addresses.md: mailparse\_rfc822\_parse\_addresses »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_msg\_parse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_msg\_parse

(PECL mailparse >= 0.9.0)

mailparse\_msg\_parse - Інкрементальне розбирає дані в буфер

### Опис

```methodsynopsis
mailparse_msg_parse(resource $mimemail, string $data): bool
```

Інкрементальне розбирає дані заданий MIME-ресурс.

Функція дозволяє обробляти файл частинами, замість того, щоб читати і обробляти відразу весь масив даних.

### Список параметрів

`mimemail`

Коректний `MIME`\-ресурс.

`data`

> **Зауваження** :
> 
> Повідомлення, що міститься в `filename`, має закінчуватися новим рядком (`CRLF`); інакше останній рядок повідомлення не буде проаналізовано.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
