---
navigation:
  - function.mailparse-msg-create.md: « mailparse\_msg\_create
  - function.mailparse-msg-extract-part.md: mailparse\_msg\_extract\_part »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_msg\_extract\_part\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_msg\_extract\_part\_file

(PECL mailparse >= 0.9.0)

mailparse\_msg\_extract\_part\_file — Вийняти/декодувати розділ із повідомленням з файлу

### Опис

```methodsynopsis
mailparse_msg_extract_part_file(resource $mimemail, mixed $filename, callable $callbackfunc = ?): string
```

Вийняти/декодувати секцію з повідомленням із зазначеного файлу.

Контент повідомлення буде декодований відповідно до кодування пересилання. Підтримуються такі кодування: base64, quoted-printable та uuencoded.

### Список параметрів

`mimemail`

Коректний `MIME`\-ресурс, створений [mailparse\_msg\_create()](function.mailparse-msg-create.md)

`filename`

Ім'я файлу чи коректний потоковий ресурс.

`callbackfunc`

Якщо задано, то в цю функцію буде надіслано вилучене повідомлення. Якщо **`null`**, то одержане повідомлення буде просто повернено.

Якщо не встановлено, то контент буде спрямований на стандартний висновок (stdout).

### Значення, що повертаються

Якщо `callbackfunc`не\*\*`null`\*\*, то поверне **`true`** у разі успішного виконання.

Якщо `callbackfunc`задана как\*\*`null`\*\*, поверне вилучену секцію повідомлення у вигляді рядка.

Поверне \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mailparse\_msg\_extract\_part()](function.mailparse-msg-extract-part.md) \- Витягти/декодувати секцію з повідомленням
-   [mailparse\_msg\_extract\_whole\_part\_file()](function.mailparse-msg-extract-whole-part-file.md) \- Витягти секцію повідомлення разом із заголовками без декодування
