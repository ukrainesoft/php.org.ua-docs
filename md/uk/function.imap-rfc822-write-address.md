---
navigation:
  - function.imap-rfc822-parse-headers.md: « imap\_rfc822\_parse\_headers
  - function.imap-savebody.md: imap\_savebody »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_rfc822\_write\_address
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_rfc822\_write\_address

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_rfc822\_write\_address — Отримує коректно сформовану адресу електронної пошти, задану ім'ям скриньки, хоста та персональною інформацією

### Опис

```methodsynopsis
imap_rfc822_write_address(string $mailbox, string $hostname, string $personal): string|false
```

Повертає поштову адресу сформовану відповідно до [» RFC2822](http://www.faqs.org/rfcs/rfc2822)

### Список параметрів

`mailbox`

Ім'я поштової скриньки. Детальніше читайте в описі [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`hostname`

Частина e-mail, що описує хост

`personal`

Ім'я власника облікового запису

### Значення, що повертаються

Повертає рядок містить поштову адресу у сформовану відповідно до [» RFC2822](http://www.faqs.org/rfcs/rfc2822)или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** imap\_rfc822\_write\_address()\*\*\*\*

```php
<?php
echo imap_rfc822_write_address("hartmut", "example.com", "Hartmut Holzgraefe");
?>
```

Результат виконання наведеного прикладу:

```
Hartmut Holzgraefe <hartmut@example.com>
```
