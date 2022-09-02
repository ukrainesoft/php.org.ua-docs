---
navigation:
  - function.imap-get-quotaroot.md: « imapgetquotaroot
  - function.imap-getmailboxes.md: imapgetmailboxes »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapgetacl
---
# imapgetacl

(PHP 5, PHP 7, PHP 8)

imapgetacl — Отримати ACL для заданої поштової скриньки

### Опис

```methodsynopsis
imap_getacl(IMAP\Connection $imap, string $mailbox): array|false
```

Повертає ACL для заданої поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі, присвяченому функції [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає асоціативний масив виду "folder" => "acl" або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapgetacl()****

```php
<?php

print_r(imap_getacl($imap, 'user.joecool'));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [asubfolder] => lrswipcda
    [anothersubfolder] => lrswipcda
)
```

### Примітки

Ця функція доступна лише під час використання бібліотеки c-client2000 або новішої.

### Дивіться також

-   [imapsetacl()](function.imap-setacl.md) - Встановлення ACL для заданої поштової скриньки
