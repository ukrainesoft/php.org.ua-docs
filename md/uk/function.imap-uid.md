---
navigation:
  - function.imap-timeout.html: « imaptimeout
  - function.imap-undelete.html: imapundelete »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapuid
---
# imapuid

(PHP 4, PHP 5, PHP 7, PHP 8)

imapuid — Отримати UID за номером повідомлення

### Опис

```methodsynopsis
imap_uid(IMAP\Connection $imap, int $message_num): int|false
```

Ця функція повертає UID для повідомлення із заданим номером. UID - це унікальний ідентифікатор, який не змінюється з часом, у той час як номер повідомлення в скриньці може змінюватися при зміні вмісту поштової скриньки.

Ця функція зворотна функції [imapmsgno()](function.imap-msgno.html)

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`message_num`

Номер повідомлення.

### Значення, що повертаються

UID заданого листа.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Примітки

> **Зауваження**
> 
> Ця функція не підтримується для поштових скриньок POP3.

### Дивіться також

-   [imapmsgno()](function.imap-msgno.html) - Отримати номер повідомлення із заданим UID
