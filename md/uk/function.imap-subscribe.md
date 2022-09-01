---
navigation:
  - function.imap-status.html: « imapstatus
  - function.imap-thread.html: imapthread »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
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

Екземпляр [IMAPConnection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки. Детальніше читай у розділі про [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imapunsubscribe()](function.imap-unsubscribe.html) - Відписатися від поштової скриньки
