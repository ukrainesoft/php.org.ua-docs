---
navigation:
  - function.mailparse-msg-extract-part.md: « mailparsemsgextractpart
  - function.mailparse-msg-free.md: mailparsemsgfree »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsemsgextractwholepartfile
---
# mailparsemsgextractwholepartfile

(PECL mailparse >= 0.9.0)

mailparsemsgextractwholepartfile — Вийняти розділ повідомлення разом із заголовками без декодування

### Опис

```methodsynopsis
mailparse_msg_extract_whole_part_file(resource $mimemail, string $filename, callable $callbackfunc = ?): string
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`mimemail`

Коректний `MIME`ресурс

`filename`

`callbackfunc`

### Значення, що повертаються

### Дивіться також

-   [mailparsemsgextractpart()](function.mailparse-msg-extract-part.md) - Вийняти/декодувати секцію із повідомленням
-   [mailparsemsgextractpartfile()](function.mailparse-msg-extract-part-file.md) - Вийняти/декодувати секцію із повідомленням із файлу
