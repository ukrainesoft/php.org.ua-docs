---
navigation:
  - function.imap-clearflag-full.html: « imapclearflagfull
  - function.imap-create.html: imapcreate »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapclose
---
# imapclose

(PHP 4, PHP 5, PHP 7, PHP 8)

imapclose — Закрити потік IMAP

### Опис

```methodsynopsis
imap_close(IMAP\Connection $imap, int $flags = 0): bool
```

Закриває IMAP-потік.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`flags`

Якщо встановлено **`CL_EXPUNGE`**, то ця функція мовчки застосує всі внесені зміни, зокрема видалить всі повідомлення, позначені для видалення. По суті зробить те саме, що і функція [imapexpunge()](function.imap-expunge.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapopen()](function.imap-open.md) - Відкриває потік IMAP до поштової скриньки
