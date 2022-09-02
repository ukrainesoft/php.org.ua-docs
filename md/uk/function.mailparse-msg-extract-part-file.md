---
navigation:
  - function.mailparse-msg-create.md: « mailparsemsgcreate
  - function.mailparse-msg-extract-part.md: mailparsemsgextractpart »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsemsgextractpartfile
---
# mailparsemsgextractpartfile

(PECL mailparse >= 0.9.0)

mailparsemsgextractpartfile — Вийняти/декодувати розділ із повідомленням з файлу

### Опис

```methodsynopsis
mailparse_msg_extract_part_file(resource $mimemail, mixed $filename, callable $callbackfunc = ?): string
```

Вийняти/декодувати секцію з повідомленням із зазначеного файлу.

Контент повідомлення буде декодований відповідно до кодування пересилання. Підтримуються такі кодування: base64, quoted-printable та uuencoded.

### Список параметрів

`mimemail`

Коректний `MIME`ресурс, створений [mailparsemsgcreate()](function.mailparse-msg-create.md)

`filename`

Ім'я файлу чи коректний потоковий ресурс.

`callbackfunc`

Якщо задано, то в цю функцію буде надіслано вилучене повідомлення. Якщо **`null`**, то одержане повідомлення буде просто повернено.

Якщо не встановлено, то контент буде спрямований на стандартний висновок (stdout).

### Значення, що повертаються

Якщо `callbackfunc` не **`null`**, то поверне **`true`** у разі успішного виконання.

Якщо `callbackfunc` задана як **`null`**, поверне вилучену секцію повідомлення у вигляді рядка.

Поверне **`false`** у разі виникнення помилки.

### Дивіться також

-   [mailparsemsgextractpart()](function.mailparse-msg-extract-part.md) - Вийняти/декодувати секцію із повідомленням
-   [mailparsemsgextractwholepartfile()](function.mailparse-msg-extract-whole-part-file.md) - Витягти секцію повідомлення разом із заголовками без декодування
