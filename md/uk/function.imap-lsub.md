---
navigation:
  - function.imap-listsubscribed.html: « imaplistsubscribed
  - function.imap-mail-compose.html: imapmailcompose »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imaplsub
---
# imaplsub

(PHP 4, PHP 5, PHP 7, PHP 8)

imaplsub — Список усіх підписаних поштових скриньок

### Опис

```methodsynopsis
imap_lsub(IMAP\Connection $imap, string $reference, string $pattern): array|false
```

Повертає масив усіх поштових скриньок, на які ви підписані.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`reference`

У `reference`, як правило, повинна бути вказана лише специфікація сервера, як описано в [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`pattern`

Визначає початок пошуку в ієрархії поштових скриньок.

Є два спеціальні символи, які можна використовувати при передачі як частину `pattern``*`'і'`%``*`' повертає всі поштові скриньки. Якщо ви передасте `pattern` як '`*`', то отримайте повний список ієрархії поштових скриньок. '`%`' поверне лише поточний рівень. '`%`', переданий як параметр `pattern`, поверне поштові скриньки лише на верхньому рівні; '`~/mail/%`' на `UW_IMAPD` поверне всі ящики в директорії ~/mail, крім тих, що знаходяться в її піддиректорії.

### Значення, що повертаються

Повертає масив усіх підписаних поштових скриньок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imaplist()](function.imap-list.md) - Прочитати список поштових скриньок
-   [imapgetmailboxes()](function.imap-getmailboxes.md) - Прочитати список поштових скриньок, повертаючи докладну інформацію щодо кожного з них
