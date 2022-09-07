---
navigation:
  - function.imap-status.md: « imapstatus
  - function.imap-thread.md: imapthread »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapsubscribe
---
# imapsubscribe

(PHP 4, PHP 5, PHP 7, PHP 8)

imapsubscribe — Передплатити поштову скриньку

### Опис

```methodsynopsis
imap_subscribe(IMAP\Connection $imap, string $mailbox): bool
```

Передплатити нову поштову скриньку.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки. Детальніше читай у розділі про [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapunsubscribe()](function.imap-unsubscribe.md) - Відписатися від поштової скриньки
