---
navigation:
  - function.imap-errors.md: « imap\_errors
  - function.imap-fetch-overview.md: imap\_fetch\_overview »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_expunge
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_expunge

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_expunge — Видалити всі позначені для видалення повідомлення

### Опис

```methodsynopsis
imap_expunge(IMAP\Connection $imap): true
```

Видаляє всі позначені для видалення повідомлення. Позначити видалення можна за допомогою функцій [imap\_delete()](function.imap-delete.md) [imap\_mail\_move()](function.imap-mail-move.md) або [imap\_setflag\_full()](function.imap-setflag-full.md)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
