---
navigation:
  - function.imap-errors.md: « imaperrors
  - function.imap-fetch-overview.md: imapfetchoverview »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapexpunge
---
# imapexpunge

(PHP 4, PHP 5, PHP 7, PHP 8)

imapexpunge — Видалити всі позначені для видалення повідомлення

### Опис

```methodsynopsis
imap_expunge(IMAP\Connection $imap): bool
```

Видаляє всі позначені для видалення повідомлення. Позначити для видалення можна за допомогою функцій [imapdelete()](function.imap-delete.md) [imapmailmove()](function.imap-mail-move.md) або [imapsetflagfull()](function.imap-setflag-full.md)

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
