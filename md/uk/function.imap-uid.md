---
navigation:
  - function.imap-timeout.md: « imap\_timeout
  - function.imap-undelete.md: imap\_undelete »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_uid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_uid

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_uid — Отримує UID за номером повідомлення

### Опис

```methodsynopsis
imap_uid(IMAP\Connection $imap, int $message_num): int|false
```

Ця функція повертає UID для повідомлення із заданим номером. UID — це унікальний ідентифікатор, який не змінюється після часу, тоді як номер повідомлення в скриньці може змінюватися при зміні вмісту поштової скриньки.

Ця функція зворотна функції [imap\_msgno()](function.imap-msgno.md)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_num`

Номер повідомлення.

### Значення, що повертаються

UID заданого листа.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Примітки

> **Зауваження** :
> 
> Ця функція не підтримується для поштових скриньок POP3.

### Дивіться також

-   [imap\_msgno()](function.imap-msgno.md) \- Отримує номер повідомлення із заданим UID
