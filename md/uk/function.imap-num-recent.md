---
navigation:
  - function.imap-num-msg.md: « imapnummsg
  - function.imap-open.md: imapopen »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapnumrecent
---
# imapnumrecent

(PHP 4, PHP 5, PHP 7, PHP 8)

imapnumrecent — Отримати кількість нових повідомлень у поточній поштовій скриньці

### Опис

```methodsynopsis
imap_num_recent(IMAP\Connection $imap): int
```

Повертає кількість нових повідомлень у поточній поштовій скриньці.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

### Значення, що повертаються

Повертає кількість нових повідомлень у поточній поштовій скриньці у вигляді цілого числа.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapnummsg()](function.imap-num-msg.md) - Отримати кількість повідомлень у поточній поштовій скриньці
-   [imapstatus()](function.imap-status.md) - Отримати інформацію про статус поштової скриньки
