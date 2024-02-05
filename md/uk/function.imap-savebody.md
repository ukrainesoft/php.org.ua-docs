---
navigation:
  - function.imap-rfc822-write-address.md: « imap\_rfc822\_write\_address
  - function.imap-scan.md: imap\_scan »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_savebody
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_savebody

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

imap\_savebody — Зберігає частину тіла повідомлення у файл

### Опис

```methodsynopsis
imap_savebody(    IMAP\Connection $imap,    resource|string|int $file,    int $message_num,    string $section = "",    int $flags = 0): bool
```

Записує частину тіла повідомлення у файл.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`file`

Шлях до файлу у вигляді рядка або відкритий за допомогою [fopen()](function.fopen.md) файловий дескриптор.

`message_num`

Номер повідомлення

`section`

Номер розділу повідомлення. Рядок цілих чисел, розділених точками, визначальна частина тіла повідомлення відповідно до специфікації IMAP4

`flags`

Бітова маска з однієї або кількох опцій:

-   \*\*`FT_UID`\*\*- The`message_num`is a UID
-   \*\*`FT_PEEK`\*\*- Не встановлювати прапор\\Seen, якщо він уже не встановлений
-   \*\*`FT_INTERNAL`\*\*- Повертати рядок у внутрішньому форматі, без перетворення кінців рядків до CRLF.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_fetchbody()](function.imap-fetchbody.md) \- Витягує конкретну секцію тіла повідомлення
