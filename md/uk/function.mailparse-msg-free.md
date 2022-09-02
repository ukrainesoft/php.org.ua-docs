---
navigation:
  - function.mailparse-msg-extract-whole-part-file.md: « mailparsemsgextractwholepartfile
  - function.mailparse-msg-get-part-data.md: mailparsemsggetpartdata »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsemsgfree
---
# mailparsemsgfree

(PECL mailparse >= 0.9.0)

mailparsemsgfree — Вивільнити MIME-ресурс

### Опис

```methodsynopsis
mailparse_msg_free(resource $mimemail): bool
```

Вивільняє `MIME`ресурс.

### Список параметрів

`mimemail`

Коректний `MIME`ресурс, створений [mailparsemsgcreate()](function.mailparse-msg-create.md) або [mailparsemsgparsefile()](function.mailparse-msg-parse-file.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mailparsemsgcreate()](function.mailparse-msg-create.md) - Створює поштовий MIME-ресурс
-   [mailparsemsgparsefile()](function.mailparse-msg-parse-file.md) - Розібрати файл
