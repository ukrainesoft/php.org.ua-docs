---
navigation:
  - function.imap-headers.md: « imap\_headers
  - function.imap-last-error.md: imap\_last\_error »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_is\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_is\_open

(PHP 8 >= 8.2.1)

imap\_is\_open — Перевіряє, чи потік IMAP все ще є коректним.

### Опис

```methodsynopsis
imap_is_open(IMAP\Connection $imap): bool
```

Перевіряє, чи потік IMAP все ще є коректним.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Повертає **`true`**, якщо потік ще коректний, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** imap\_is\_open()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org:143}INBOX", "username", "password") or die(implode(", ", imap_errors()));
imap_is_open($mbox);
// ...
?>
```
