---
navigation:
  - function.mailparse-msg-extract-part-file.html: « mailparsemsgextractpartfile
  - function.mailparse-msg-extract-whole-part-file.html: mailparsemsgextractwholepartfile »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsemsgextractpart
---
# mailparsemsgextractpart

(PECL mailparse >= 0.9.0)

mailparsemsgextractpart — Вийняти/декодувати розділ із повідомленням

### Опис

```methodsynopsis
mailparse_msg_extract_part(resource $mimemail, string $msgbody, callable $callbackfunc = ?): void
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`mimemail`

Коректний `MIME`ресурс

`msgbody`

`callbackfunc`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mailparsemsgextractpartfile()](function.mailparse-msg-extract-part-file.html) - Вийняти/декодувати секцію з повідомленням із файлу
-   [mailparsemsgextractwholepartfile()](function.mailparse-msg-extract-whole-part-file.html) - Витягти секцію повідомлення разом із заголовками без декодування
