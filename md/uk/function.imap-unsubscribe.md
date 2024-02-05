---
navigation:
  - function.imap-undelete.md: « imap\_undelete
  - function.imap-utf7-decode.md: imap\_utf7\_decode »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_unsubscribe
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_unsubscribe

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_unsubscribe — Відписує від поштової скриньки

### Опис

```methodsynopsis
imap_unsubscribe(IMAP\Connection $imap, string $mailbox): bool
```

Відписатися від поштової скриньки `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки. Детальніше дивіться в розділі про [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_subscribe()](function.imap-subscribe.md) \- Підписує на поштову скриньку
