---
navigation:
  - function.imap-get-quotaroot.md: « imap\_get\_quotaroot
  - function.imap-getmailboxes.md: imap\_getmailboxes »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_getacl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_getacl

(PHP 5, PHP 7, PHP 8)

imap\_getacl — Отримує ACL для заданої поштової скриньки

### Опис

```methodsynopsis
imap_getacl(IMAP\Connection $imap, string $mailbox): array|false
```

Повертає ACL для заданої поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі, присвяченому функції [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає асоціативний масив виду "folder" => "acl" або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Приклад #1 Приклад використання** imap\_getacl()\*\*\*\*

```php
<?php

print_r(imap_getacl($imap, 'user.joecool'));

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [imap\_setacl()](function.imap-setacl.md) \- Встановлює ACL для заданої поштової скриньки
