---
navigation:
  - function.mailparse-msg-extract-whole-part-file.md: « mailparse\_msg\_extract\_whole\_part\_file
  - function.mailparse-msg-get-part-data.md: mailparse\_msg\_get\_part\_data »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_msg\_free
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_msg\_free

(PECL mailparse >= 0.9.0)

mailparse\_msg\_free — Вивільнити MIME-ресурс

### Опис

```methodsynopsis
mailparse_msg_free(resource $mimemail): bool
```

Вивільняє `MIME`\-ресурс.

### Список параметрів

`mimemail`

Коректний `MIME`\-ресурс, створений [mailparse\_msg\_create()](function.mailparse-msg-create.md) або [mailparse\_msg\_parse\_file()](function.mailparse-msg-parse-file.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mailparse\_msg\_create()](function.mailparse-msg-create.md) \- Створює поштовий MIME-ресурс
-   [mailparse\_msg\_parse\_file()](function.mailparse-msg-parse-file.md) \- Розібрати файл
