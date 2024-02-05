---
navigation:
  - function.ezmlm-hash.md: « ezmlm\_hash
  - book.mailparse.md: Mailparse »
  - index.md: PHP Manual
  - ref.mail.md: Пошта
title: mail
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mail

(PHP 4, PHP 5, PHP 7, PHP 8)

mail — Надсилає електронну пошту

### Опис

```methodsynopsis
mail(    string $to,    string $subject,    string $message,    array|string $additional_headers = [],    string $additional_params = ""): bool
```

Надсилає електронну пошту.

### Список параметрів

`to`

Одержувач або одержувачі листа.

Формат строки по правилам стандарта[» RFC 2822](http://www.faqs.org/rfcs/rfc2822). Приклади:

-   [user@example.com](mailto:user@example.com)
-   [user@example.com](mailto:user@example.com) [anotheruser@example.com](mailto:anotheruser@example.com)
-   User[user@example.com](mailto:user@example.com)
-   User[user@example.com](mailto:user@example.com), Another User[anotheruser@example.com](mailto:anotheruser@example.com)

`subject`

Тема листа, що надсилається.

**Застереження**

Тема должна удовлетворять правилам стандарта[» RFC 2047](http://www.faqs.org/rfcs/rfc2047)

`message`

Надіслане повідомлення.

Кожен рядок має бути відокремлений комбінацією символом CRLF (\\r\\n). Рядки не повинні бути довшими за 70 символів.

**Застереження**

(Тільки для Windows) Якщо при прямому зверненні PHP до SMTP-сервера на початку рядка виявлена ​​точка, що позначає кінець пропозиції, вона видаляється. Щоб протидіяти цьому, ці входження замінюють подвійною точкою.

```php
<?php

$text = str_replace("\n.", "\n..", $text);

?>
```

`additional_headers` (Необов'язковий)

Рядок або масив, які будуть вставлені в кінець заголовка листа.

Найчастіше користуються, щоб додати додаткові заголовки (From, Cc, і Bcc). Додаткові заголовки поділяють комбінацією символів CRLF (\\r\\n). Якщо у складанні заголовка беруть участь зовнішні дані, їх очищають, щоб унеможливити впровадження небажаних заголовків.

Якщо передано масив, його ключі будуть іменами заголовка, а значення значеннями.

> **Зауваження** :
> 
> Отправляемое письмо*повинно* містити заголовок `From`Его устанавливают через параметр`additional_headers`или задают значение по умолчанию в файле php.ini.
> 
> Якщо заголовок відсутній, буде видано повідомлення про помилку на кшталт `Warning: mail(): "sendmail_from" not set in php.ini or custom "From:" header missing`Заголовок`From` також визначає заголовок `Return-Path` під час прямого надсилання через SMTP-сервер (лише Windows).

> **Зауваження** :
> 
> Якщо повідомлення не надсилаються, намагаються вказати лише символ LF (\\n). Деякі агенти пересилання повідомлень Unix (особливо [» qmail](http://cr.yp.to/qmail.md)) автоматично замінюють символ перекладу рядка LF на комбінацію символів CRLF (що подвоює символ повернення каретки CR, якщо було зазначено CRLF). Цей захід обирають у крайньому випадку, оскільки він не відповідає стандарту [» RFC 2822](http://www.faqs.org/rfcs/rfc2822)

`additional_params` (Необов'язковий)

Параметр`additional_params` задають, щоб передати додаткові прапори як аргументів командного рядка для програми, налаштованої директиві `sendmail_path` для надсилання листів. Наприклад, цим користуються при надсиланні листа агентом sendmail з аргументом `-f`, щоб встановити адресу відправника конверта.

Параметр автоматично екранується функцією [escapeshellcmd()](function.escapeshellcmd.md), щоб запобігти виконанню команди. Функція [escapeshellcmd()](function.escapeshellcmd.md) виключає виконання команди, але дозволяє додаткові параметри. З міркувань безпеки рекомендовано очищати цей параметр, щоб не допустити додавання небажаних параметрів до команди командної оболонки.

Оскільки функція [escapeshellcmd()](function.escapeshellcmd.md) обробляє параметр автоматично, частину символів, дозволених інтернет-стандартами як адреси електронної пошти, не можна вказувати. Функція **mail()** не дозволяє такі символи, тому в програмах, в яких вони потрібні, рекомендовано використовувати альтернативи для їх надсилання (наприклад, фреймворки або бібліотеки).

Користувач, від імені якого запущено веб-сервер, повинен бути доданий в конфігурацію агента sendmail як довіреного користувача, щоб запобігти додаванню заголовка X-Warning в повідомлення, коли відправник конверта встановлено через аргумент (-f). Для користувачів агента sendmail це файл /etc/mail/trusted-users.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо лист був прийнятий для передачі, інакше **`false`**

Те, що лист було прийнято передачі, значить, що він досягне одержувача.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Параметр`additional_headers` тепер приймає масив. |

### Приклади

**Приклад #1 Надсилання листа.**

Виклик функції **mail()** для надсилання простого листа:

```php
<?php

// Сообщение
$message = "Line 1\r\nLine 2\r\nLine 3";

// На случай если какая-то строка письма длиннее 70 символов, вызовем функцию wordwrap()
$message = wordwrap($message, 70, "\r\n");

// Отправляем
mail('caffeinated@example.com', 'My Subject', $message);

?>
```

**Приклад #2 Надсилання листа з додатковими заголовками.**

Додавання простих заголовків, які повідомляють поштовому агенту адреси From та Reply-To:

```php
<?php

$to      = 'nobody@example.com';
$subject = 'the subject';
$message = 'hello';
$headers = 'From: webmaster@example.com' . "\r\n" .
    'Reply-To: webmaster@example.com' . "\r\n" .
    'X-Mailer: PHP/' . phpversion();

mail($to, $subject, $message, $headers);

?>
```

**Приклад #3 Надсилання листа з додатковими заголовками, переданими масивом**

У цьому прикладі надсилається той же лист, що і в прикладі вище, але додаткові заголовки задаються масивом (доступно з PHP 7.2.0).

```php
<?php

$to      = 'nobody@example.com';
$subject = 'the subject';
$message = 'hello';
$headers = array(
    'From' => 'webmaster@example.com',
    'Reply-To' => 'webmaster@example.com',
    'X-Mailer' => 'PHP/' . phpversion()
);

mail($to, $subject, $message, $headers);

?>
```

**Приклад #4 Надсилання листа з додатковими аргументами командного рядка.**

Параметр`additional_params` вказують, щоб передати додатковий аргумент програмі, налаштованій у директиві `sendmail_path`для отправки писем.

```php
<?php

mail('nobody@example.com', 'the subject', 'the message', null,
   '-fwebmaster@example.com');

?>
```

**Приклад #5 Надсилання HTML-повідомлення**

функцією **mail()** можна також надіслати електронний лист у форматі HTML.

```php
<?php

// Несколько получателей
$to = 'johny@example.com, sally@example.com'; // Обратите внимание на запятую

// Тема письма
$subject = 'Birthday Reminders for August';

// Текст письма
$message = '
<html>
<head>
  <title>Birthday Reminders for August</title>
</head>
<body>
  <p>Here are the birthdays upcoming in August!</p>
  <table>
    <tr>
      <th>Person</th><th>Day</th><th>Month</th><th>Year</th>
    </tr>
    <tr>
      <td>Johny</td><td>10th</td><td>August</td><td>1970</td>
    </tr>
    <tr>
      <td>Sally</td><td>17th</td><td>August</td><td>1973</td>
    </tr>
  </table>
</body>
</html>
';

// Для отправки HTML-письма должен быть установлен заголовок Content-type
$headers[] = 'MIME-Version: 1.0';
$headers[] = 'Content-type: text/html; charset=iso-8859-1';

// Дополнительные заголовки
$headers[] = 'To: Mary <mary@example.com>, Kelly <kelly@example.com>';
$headers[] = 'From: Birthday Reminder <birthday@example.com>';
$headers[] = 'Cc: birthdayarchive@example.com';
$headers[] = 'Bcc: birthdaycheck@example.com';

// Отправляем
mail($to, $subject, $message, implode("\r\n", $headers));

?>
```

> **Зауваження** :
> 
> Для надсилання HTML-повідомлень або інших складних електронних листів рекомендовано встановлення PEAR-пакету [» PEAR::Mail\_Mime](https://pear.php.net/package/Mail_Mime)

### Примітки

> **Зауваження** :
> 
> Реалізація SMTP (лише Windows) функції **mail()** Windows багато в чому відрізняється від реалізації в агенті sendmail. По-перше, вона не використовує локальну програму для складання листів, а працює безпосередньо з сокетами, що означає, що необхідний поштовий агент (`MTA`), що очікує з'єднань на сокеті (який може бути як на локальній, чи localhost, так і на віддаленій машині).
> 
> По-друге, додаткові заголовки на кшталт: `From:` `Cc:` `Bcc:`и`Date:` інтерпретуються насамперед **не** поштовим агентом `MTA`, а PHP.
> 
> Тому параметр `to` не має бути адресою виду "Something [someone@example.com](mailto:someone@example.com)Команда mail може неправильно інтерпретувати цю адресу під час передачі даних поштовим агентом MTA.

> **Зауваження** :
> 
> Функция**mail()** не рекомендована для надсилання великої кількості листів у циклі. Функція відкриває та закриває SMTP-сокет для кожного листа, що не дуже ефективно.
> 
> Для надсилання великої кількості повідомлень зверніть увагу на пакети [» PEAR::Mail](https://pear.php.net/package/Mail) і [» PEAR::Mail\_Queue](https://pear.php.net/package/Mail_Queue)

> **Зауваження** :
> 
> Корисні RFC: [» RFC 1896](http://www.faqs.org/rfcs/rfc1896) [» RFC 2045](http://www.faqs.org/rfcs/rfc2045) [» RFC 2046](http://www.faqs.org/rfcs/rfc2046) [» RFC 2047](http://www.faqs.org/rfcs/rfc2047) [» RFC 2048](http://www.faqs.org/rfcs/rfc2048) [» RFC 2049](http://www.faqs.org/rfcs/rfc2049) і [» RFC 2822](http://www.faqs.org/rfcs/rfc2822)

### Дивіться також

-   [mb\_send\_mail()](function.mb-send-mail.md) \- Надсилає закодований електронний лист
-   [imap\_mail()](function.imap-mail.md) \- Надсилає повідомлення
-   [» PEAR::Mail](https://pear.php.net/package/Mail)
-   [» PEAR::Mail\_Mime](https://pear.php.net/package/Mail_Mime)
