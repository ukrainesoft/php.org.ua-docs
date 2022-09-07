---
navigation:
  - function.imap-rfc822-write-address.md: « imaprfc822writeaddress
  - function.imap-scan.md: imapscan »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapsavebody
---
# imapsavebody

(PHP 5> = 5.1.3, PHP 7, PHP 8)

imapsavebody — Зберегти частину тіла повідомлення у файл

### Опис

```methodsynopsis
imap_savebody(    IMAP\Connection $imap,    resource|string|int $file,    int $message_num,    string $section = "",    int $flags = 0): bool
```

Записує частину тіла повідомлення у файл.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`file`

Шлях до файлу у вигляді рядка або відкритий за допомогою [fopen()](function.fopen.md) файловий дескриптор.

`message_num`

Номер повідомлення

`section`

Номер розділу повідомлення. Рядок цілих чисел, розділених точками, визначальна частина тіла повідомлення відповідно до специфікації IMAP4

`flags`

Бітова маска з однієї або кількох опцій:

-   **`FT_UID`** - The `message_num` is a UID
-   **`FT_PEEK`** - Не встановлювати прапор Seen, якщо його вже не встановлено
-   **`FT_INTERNAL`** - Повертати рядок у внутрішньому форматі, без перетворення кінців рядків до CRLF.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapfetchbody()](function.imap-fetchbody.md) - Витягти конкретну секцію тіла повідомлення
