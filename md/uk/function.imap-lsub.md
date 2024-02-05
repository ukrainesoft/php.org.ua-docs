---
navigation:
  - function.imap-listsubscribed.md: « imap\_listsubscribed
  - function.imap-mail-compose.md: imap\_mail\_compose »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_lsub
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_lsub

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_lsub — Отримує список усіх поштових скриньок, на які оформлена передплата

### Опис

```methodsynopsis
imap_lsub(IMAP\Connection $imap, string $reference, string $pattern): array|false
```

Повертає масив усіх поштових скриньок, на які ви підписані.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`reference`

В`reference`, як правило, повинна бути вказана лише специфікація сервера, як описано в [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`pattern`

Визначає початок пошуку в ієрархії поштових скриньок.

Є два спеціальні символи, які можна використовувати при передачі як частину `pattern`: '`*`'і'`%`'. '`*`' повертає всі поштові скриньки. Якщо ви передасте `pattern` як '`*`', то отримайте повний список ієрархії поштових скриньок. '`%`' поверне лише поточний рівень. '`%`', переданий як параметр `pattern`, поверне поштові скриньки лише на верхньому рівні; '`~/mail/%`' на `UW_IMAPD` поверне всі ящики в директорії ~/mail, крім тих, що знаходяться в її піддиректорії.

### Значення, що повертаються

Повертає масив усіх підписаних поштових скриньок або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_list()](function.imap-list.md) \- Читає список поштових скриньок
-   [imap\_getmailboxes()](function.imap-getmailboxes.md) \- Читає список поштових скриньок, повертаючи докладну інформацію щодо кожного з них
