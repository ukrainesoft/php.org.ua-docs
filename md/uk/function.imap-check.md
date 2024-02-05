---
navigation:
  - function.imap-bodystruct.md: « imap\_bodystruct
  - function.imap-clearflag-full.md: imap\_clearflag\_full »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_check
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_check

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_check — Перевіряє поточну поштову скриньку

### Опис

```methodsynopsis
imap_check(IMAP\Connection $imap): stdClass|false
```

Перевіряє інформацію поточної поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Повертає об'єкт із такими властивостями:

-   \*\*`Date`\*\*- поточний системний час у відповідному форматі[» RFC2822](http://www.faqs.org/rfcs/rfc2822)
-   \*\*`Driver`\*\*- протокол, який використовується для доступу до поштової скриньки: POP3, IMAP, NNTP
-   \*\*`Mailbox`\*\*- ім'я поштової скриньки
-   \*\*`Nmsgs`\*\*- кількість повідомлень
-   \*\*`Recent`\*\*- кількість нових повідомлень

У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Пример #1 Пример использования**imap\_check()\*\*\*\*

```php
<?php

$imap = imap_check($imap_stream);
var_dump($imap);

?>
```

Висновок наведеного прикладу буде схожим на:

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
