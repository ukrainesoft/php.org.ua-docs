---
navigation:
  - function.imap-delete.html: « imapdelete
  - function.imap-errors.html: imaperrors »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapdeletemailbox
---
# imapdeletemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imapdeletemailbox — Видалити поштову скриньку

### Опис

```methodsynopsis
imap_deletemailbox(IMAP\Connection $imap, string $mailbox): bool
```

Видаляє поштову скриньку `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`mailbox`

Ім'я ящика. Детальніше читайте в описі [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapcreatemailbox()](function.imap-createmailbox.html) - Створити нову поштову скриньку
-   [imaprenamemailbox()](function.imap-renamemailbox.html) - Перейменувати поштову скриньку
-   [imapopen()](function.imap-open.html) - Відкриває потік IMAP до поштової скриньки формату `mbox`
