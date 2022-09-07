---
navigation:
  - function.imap-undelete.md: « imapundelete
  - function.imap-utf7-decode.md: imaputf7decode »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapunsubscribe
---
# imapunsubscribe

(PHP 4, PHP 5, PHP 7, PHP 8)

imapunsubscribe — Відписатися від поштової скриньки

### Опис

```methodsynopsis
imap_unsubscribe(IMAP\Connection $imap, string $mailbox): bool
```

Відписатися від поштової скриньки `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки. Детальніше дивіться в розділі про [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapsubscribe()](function.imap-subscribe.md) - Підписатися на поштову скриньку
