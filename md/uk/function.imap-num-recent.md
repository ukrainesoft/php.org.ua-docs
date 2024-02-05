---
navigation:
  - function.imap-num-msg.md: « imap\_num\_msg
  - function.imap-open.md: imap\_open »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_num\_recent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_num\_recent

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_num\_recent — Отримує кількість нових повідомлень у поточній поштовій скриньці

### Опис

```methodsynopsis
imap_num_recent(IMAP\Connection $imap): int
```

Повертає кількість нових повідомлень у поточній поштовій скриньці.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Повертає кількість нових повідомлень у поточній поштовій скриньці у вигляді цілого числа.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_num\_msg()](function.imap-num-msg.md) \- Отримує кількість повідомлень у поточній поштовій скриньці
-   [imap\_status()](function.imap-status.md) \- Отримує інформацію щодо статусу поштової скриньки
