---
navigation:
  - function.imap-mime-header-decode.md: « imap\_mime\_header\_decode
  - function.imap-mutf7-to-utf8.md: imap\_mutf7\_to\_utf8 »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_msgno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_msgno

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_msgno — Отримує номер повідомлення із заданим UID

### Опис

```methodsynopsis
imap_msgno(IMAP\Connection $imap, int $message_uid): int
```

Повертає номер повідомлення для зазначеного у параметрі `message_uid` ідентифікатор.

Ця функція зворотна до [imap\_uid()](function.imap-uid.md)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_uid`

UID повідомлення

### Значення, що повертаються

Повертає номер повідомлення для зазначеного `message_uid`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_uid()](function.imap-uid.md) \- Отримує UID за номером повідомлення
