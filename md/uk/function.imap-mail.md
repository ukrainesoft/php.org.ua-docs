---
navigation:
  - function.imap-mail-move.md: « imap\_mail\_move
  - function.imap-mailboxmsginfo.md: imap\_mailboxmsginfo »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_mail
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_mail

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_mail — Надсилає повідомлення

### Опис

```methodsynopsis
imap_mail(    string $to,    string $subject,    string $message,    ?string $additional_headers = null,    ?string $cc = null,    ?string $bcc = null,    ?string $return_path = null): bool
```

Ця функція дозволяє надсилати повідомлення з коректною обробкою одержувачів Cc та Bcc.

Параметри `to` `cc`и`bcc` - рядки, які будуть розібрані відповідно до [» RFC822](http://www.faqs.org/rfcs/rfc822)

### Список параметрів

`to`

Одержувач

`subject`

Тема листа

`message`

Тело письма, смотрите[imap\_mail\_compose()](function.imap-mail-compose.md)

`additional_headers`

Рядок з додатковими заголовками

`cc`

`bcc`

Получатели`bcc` отримають листа, але не будуть вказані в заголовках.

`return_path`

Використовуйте цей параметр для вказівки зворотної адреси для надсилання звіту у разі невдалої доставки. Це зручно, коли PHP використовується як поштовий клієнт кількома користувачами.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `additional_headers` `cc` `bcc`и`return_path` тепер допускають значення null. |

### Дивіться також

-   [mail()](function.mail.md) \- Надсилає електронну пошту
-   [imap\_mail\_compose()](function.imap-mail-compose.md) \- Створює MIME-повідомлення на основі заданих обгортки та тіла
