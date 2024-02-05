---
navigation:
  - function.imap-reopen.md: « imap\_reopen
  - function.imap-rfc822-parse-headers.md: imap\_rfc822\_parse\_headers »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_rfc822\_parse\_adrlist
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_rfc822\_parse\_adrlist

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_rfc822\_parse\_adrlist — Розбирає адресний рядок

### Опис

```methodsynopsis
imap_rfc822_parse_adrlist(string $string, string $default_hostname): array
```

Розбирає адресний рядок відповідно до [» RFC2822](http://www.faqs.org/rfcs/rfc2822) для кожної адреси.

### Список параметрів

`string`

Рядок з адресами

`default_hostname`

Ім'я хоста за замовчуванням

### Значення, що повертаються

Повертає масив об'єктів з такими властивостями:

-   mailbox - ім'я скриньки (користувача)
-   host - ім'я хоста
-   personal - персональне ім'я
-   adl - "at-domain-list". Не використовується.

### Приклади

**Пример #1 Пример использования**imap\_rfc822\_parse\_adrlist()\*\*\*\*

```php
<?php

$address_string = "Joe Doe <doe@example.com>, postmaster@example.com, root";
$address_array  = imap_rfc822_parse_adrlist($address_string, "example.com");
if (!is_array($address_array) || count($address_array) < 1) {
    die("something is wrong\n");
}

foreach ($address_array as $id => $val) {
    echo "# $id\n";
    echo "  mailbox : " . $val->mailbox . "\n";
    echo "  host    : " . $val->host . "\n";
    echo "  personal: " . $val->personal . "\n";
    echo "  adl     : " . $val->adl . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
# 0
  mailbox : doe
  host    : example.com
  personal: Joe Doe
  adl     :
# 1
  mailbox : postmaster
  host    : example.com
  personal:
  adl     :
# 2
  mailbox : root
  host    : example.com
  personal:
  adl     :
```

### Дивіться також

-   [imap\_rfc822\_parse\_headers()](function.imap-rfc822-parse-headers.md) \- Розбирає рядок заголовка листа
