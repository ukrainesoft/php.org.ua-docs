---
navigation:
  - function.imap-mutf7-to-utf8.html: « imapmutf7тоutf8
  - function.imap-num-recent.html: imapnumrecent »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
title: imapnummsg
---
# imapnummsg

(PHP 4, PHP 5, PHP 7, PHP 8)

imapnummsg — Отримати кількість повідомлень у поточній поштовій скриньці

### Опис

```methodsynopsis
imap_num_msg(IMAP\Connection $imap): int|false
```

Повертає кількість повідомлень у поточній поштовій скриньці.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

### Значення, що повертаються

Повертає кількість повідомлень у поточній поштовій скриньці у вигляді цілого числа. У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imapnumrecent()](function.imap-num-recent.html) - Отримати кількість нових повідомлень у поточній поштовій скриньці
-   [imapstatus()](function.imap-status.html) - Отримати інформацію про статус поштової скриньки
