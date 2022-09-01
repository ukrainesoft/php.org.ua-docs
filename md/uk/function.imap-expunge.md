---
navigation:
  - function.imap-errors.html: « imaperrors
  - function.imap-fetch-overview.html: imapfetchoverview »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
title: imapexpunge
---
# imapexpunge

(PHP 4, PHP 5, PHP 7, PHP 8)

imapexpunge — Видалити всі позначені для видалення повідомлення

### Опис

```methodsynopsis
imap_expunge(IMAP\Connection $imap): bool
```

Видаляє всі позначені для видалення повідомлення. Позначити для видалення можна за допомогою функцій [imapdelete()](function.imap-delete.html) [imapmailmove()](function.imap-mail-move.html) або [imapsetflagfull()](function.imap-setflag-full.html)

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
