---
navigation:
  - function.imap-mail-compose.md: « imap\_mail\_compose
  - function.imap-mail-move.md: imap\_mail\_move »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_mail\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_mail\_copy

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_mail\_copy — Копіює повідомлення до вказаної поштової скриньки

### Опис

```methodsynopsis
imap_mail_copy(    IMAP\Connection $imap,    string $message_nums,    string $mailbox,    int $flags = 0): bool
```

Копіює задані у параметрі `message_nums` листи у вказану поштову скриньку.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_nums`

`message_nums` - це діапазон, а не просто номери повідомлень (як визначено в [» RFC2060](http://www.faqs.org/rfcs/rfc2060)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі, присвяченому функції [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`flags`

`flags` - бітова маска однієї або кількох констант:

-   \*\*`CP_UID`\*\*- означає, що у першому параметрі не номери повідомлень, які UID.
-   \*\*`CP_MOVE`\*\*- Видалити оригінальні повідомлення після копіювання. Якщо цей прапор встановлено, функція поводиться ідентично до функції[imap\_mail\_move()](function.imap-mail-move.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_mail\_move()](function.imap-mail-move.md) \- Переміщує вказані повідомлення у вказану поштову скриньку
