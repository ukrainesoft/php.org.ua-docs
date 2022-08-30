Отримати коректно сформовану e-mail адресу, задану ім'ям скриньки, хоста та персональною інформацією

-   [« imaprfc822parseheaders](function.imap-rfc822-parse-headers.html)
    
-   [imapsavebody »](function.imap-savebody.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати коректно сформовану e-mail адресу, задану ім'ям скриньки, хоста та персональною інформацією
    

# imaprfc822writeaddress

(PHP 4, PHP 5, PHP 7, PHP 8)

imaprfc822writeaddress — Отримати коректно сформовану e-mail адресу, задану ім'ям скриньки, хоста та персональною інформацією

### Опис

```methodsynopsis
imap_rfc822_write_address(string $mailbox, string $hostname, string $personal): string|false
```

Повертає поштову адресу сформовану відповідно до [» RFC2822](http://www.faqs.org/rfcs/rfc2822)

### Список параметрів

`mailbox`

Ім'я поштової скриньки. Детальніше читайте в описі [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`hostname`

Частина e-mail, що описує хост

`personal`

Ім'я власника облікового запису

### Значення, що повертаються

Повертає рядок містить поштову адресу у сформовану відповідно до [» RFC2822](http://www.faqs.org/rfcs/rfc2822) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **imaprfc822writeaddress()****

```php
<?php
echo imap_rfc822_write_address("hartmut", "example.com", "Hartmut Holzgraefe");
?>
```

Результат виконання цього прикладу:

```
Hartmut Holzgraefe <hartmut@example.com>
```