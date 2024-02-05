---
navigation:
  - function.imap-status.md: « imap\_status
  - function.imap-thread.md: imap\_thread »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_subscribe
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_subscribe

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_subscribe — Підписує на поштову скриньку

### Опис

```methodsynopsis
imap_subscribe(IMAP\Connection $imap, string $mailbox): bool
```

Підписує на нову поштову скриньку.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки. Детальніше читай у розділі про [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_unsubscribe()](function.imap-unsubscribe.md) \- відписує від поштової скриньки
