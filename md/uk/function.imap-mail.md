Надіслати email

-   [« imapmailmove](function.imap-mail-move.html)
    
-   [imapmailboxmsginfo »](function.imap-mailboxmsginfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Надіслати email
    

# imapmail

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmail — Надіслати email

### Опис

```methodsynopsis
imap_mail(    string $to,    string $subject,    string $message,    ?string $additional_headers = null,    ?string $cc = null,    ?string $bcc = null,    ?string $return_path = null): bool
```

Ця функція дозволяє надсилати повідомлення з коректною обробкою одержувачів Cc та Bcc.

Параметри `to` `cc` і `bcc` - рядки, які будуть розібрані відповідно до [» RFC822](http://www.faqs.org/rfcs/rfc822)

### Список параметрів

`to`

Одержувач

`subject`

Тема листа

`message`

Тіло листа, дивіться [imapmailcompose()](function.imap-mail-compose.html)

`additional_headers`

Рядок з додатковими заголовками

`cc`

`bcc`

Одержувачі `bcc` отримають листа, але не будуть вказані в заголовках.

`return_path`

Використовуйте цей параметр для вказівки зворотної адреси для надсилання звіту у разі невдалої доставки. Це зручно, коли PHP використовується як поштовий клієнт кількома користувачами.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `additional_headers` `cc` `bcc` і `return_path` тепер допускають значення null. |

### Дивіться також

-   [mail()](function.mail.html) - Надсилає електронну пошту
-   [imapmailcompose()](function.imap-mail-compose.html) - Створити MIME-повідомлення на основі заданих обгортки та тіла