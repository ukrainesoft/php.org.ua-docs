---
navigation:
  - function.imap-mail-compose.md: « imapmailcompose
  - function.imap-mail-move.md: imapmailmove »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapmailcopy
---
# imapmailcopy

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmailcopy — Скопіювати повідомлення до вказаної поштової скриньки

### Опис

```methodsynopsis
imap_mail_copy(    IMAP\Connection $imap,    string $message_nums,    string $mailbox,    int $flags = 0): bool
```

Копіює задані в `message_nums` листи у вказану поштову скриньку.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`message_nums`

`message_nums` - це діапазон, а не просто номери повідомлень (як визначено в [» RFC2060](http://www.faqs.org/rfcs/rfc2060)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі, присвяченому функції [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`flags`

`flags` - бітова маска однієї або кількох констант:

-   **`CP_UID`** - означає, що у першому параметрі не номери повідомлень, які UID.
-   **`CP_MOVE`** - Видалити оригінальні повідомлення після копіювання. Якщо цей прапор встановлено, функція поводиться ідентично до функції [imapmailmove()](function.imap-mail-move.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapmailmove()](function.imap-mail-move.md) - Перемістити вказані повідомлення у вказану поштову скриньку
