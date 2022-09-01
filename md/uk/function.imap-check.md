---
navigation:
  - function.imap-bodystruct.html: « imapbodystruct
  - function.imap-clearflag-full.html: imapclearflagfull »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapcheck
---
# imapcheck

(PHP 4, PHP 5, PHP 7, PHP 8)

imapcheck — Перевірити поточну поштову скриньку

### Опис

```methodsynopsis
imap_check(IMAP\Connection $imap): stdClass|false
```

Перевіряє інформацію поточної поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

### Значення, що повертаються

Повертає об'єкт із такими властивостями:

-   **`Date`** - поточний системний час у відповідному форматі [» RFC2822](http://www.faqs.org/rfcs/rfc2822)
-   **`Driver`** - протокол, який використовується для доступу до поштової скриньки: POP3, IMAP, NNTP
-   **`Mailbox`** - ім'я поштової скриньки
-   **`Nmsgs`** - кількість повідомлень
-   **`Recent`** - кількість нових повідомлень

У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapcheck()****

```php
<?php

$imap = imap_check($imap_stream);
var_dump($imap);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)(5) {
  ["Date"]=>
  string(37) "Wed, 10 Dec 2003 17:56:54 +0100 (CET)"
  ["Driver"]=>
  string(4) "imap"
  ["Mailbox"]=>
  string(54)
  "{www.example.com:143/imap/user="foo@example.com"}INBOX"
  ["Nmsgs"]=>
  int(1)
  ["Recent"]=>
  int(0)
}
```
