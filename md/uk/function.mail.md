Надсилає електронну пошту

-   [« ezmlm\_hash](function.ezmlm-hash.html)
    
-   [Mailparse »](book.mailparse.html)
    
-   [PHP Manual](index.html)
    
-   [Почта](ref.mail.html)
    
-   Надсилає електронну пошту
    

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

Формат цього параметра має відповідати [» RFC 2822](http://www.faqs.org/rfcs/rfc2822). Декілька прикладів:

-   [user@example.com](mailto:user@example.com)
-   [user@example.com](mailto:user@example.com) [anotheruser@example.com](mailto:anotheruser@example.com)
-   User [user@example.com](mailto:user@example.com)
-   User [user@example.com](mailto:user@example.com), Another User [anotheruser@example.com](mailto:anotheruser@example.com)

`subject`

Тема листа, що надсилається.

**Застереження**

Тема має відповідати [» RFC 2047](http://www.faqs.org/rfcs/rfc2047)

`message`

Надіслане повідомлення.

Кожен рядок має бути відокремлений символом CRLF (рn). Рядки не повинні бути довшими за 70 символів.

**Застереження**

(Тільки для Windows) Якщо PHP передає дані безпосередньо SMTP-серверу і на початку рядка стоїть точка, вона буде видалена. Щоб уникнути цього, замініть всі такі точки на дві.

```php
<?php
$text = str_replace("\n.", "\n..", $text);
?>
```

`additional_headers` (Необов'язковий)

Рядок або масив, які будуть вставлені в кінець заголовків листа, що відправляються.

Зазвичай використовується додавання додаткових заголовків (From, Cc, and Bcc). Декілька додаткових заголовків повинні бути розділені CRLF (рn). Якщо для складання цього заголовка використовуються зовнішні дані, то вони повинні бути перевірені для уникнення небажаних ін'єкцій заголовків.

Якщо передано масив, його ключі будуть іменами заголовка, а значення значеннями.

> **Зауваження**
> 
> До PHP 5.4.42 та 5.5.27, параметр `additional_headers` не мав захисту від ін'єкції. Так що користувачі повинні переконатися, що заголовки, що передаються, безпечні і містять тільки заголовки. тобто. не містять кілька перекладів рядків поспіль, що стартує тіло повідомлення.

> **Зауваження**
> 
> При надсиланні лист *повинно* містити заголовок `From`. Він може бути встановлений за допомогою параметра `additional_headers`, або значення за промовчанням може бути встановлене в php.ini.
> 
> Якщо заголовок відсутній, буде згенеровано повідомлення про помилку виду `Warning: mail(): "sendmail_from" not set in php.ini or custom "From:" header missing`. Заголовок `From` також визначає заголовок `Return-Path` при надсиланні безпосередньо через SMTP (лише Windows).

> **Зауваження**
> 
> Якщо повідомлення не надсилаються, спробуйте використовувати лише LF (n). Деякі агенти пересилання повідомлень Unix (особливо [» qmail](http://cr.yp.to/qmail.html)) автоматично замінюють LF на CRLF (що призводить до подвійного CR, якщо використовувалося CRLF). Використовуйте цей захід у крайньому випадку, оскільки це порушує [» RFC 2822](http://www.faqs.org/rfcs/rfc2822)

`additional_params` (Необов'язковий)

Параметр `additional_params` може бути використаний для передачі додаткових прапорів у вигляді аргументів командного рядка для програми, налаштованої для надсилання листів, зазначеної директивою `sendmail_path`. Наприклад, можна встановити відправника листа під час використання sendmail за допомогою опції `-f`

Параметр автоматично екранується функцією [escapeshellcmd()](function.escapeshellcmd.html)щоб не допустити виконання команд. Але [escapeshellcmd()](function.escapeshellcmd.html) дозволяє додавати додаткові параметри. З метою безпеки рекомендується перевіряти та очищати цей параметр.

Так як [escapeshellcmd()](function.escapeshellcmd.html) застосовується автоматично, то не можна використовувати деякі символи, допустимі для використання в email-адресах деякими RFC . **mail()** не допускає такі символи, тому в програмах, в яких вони потрібні, рекомендується використовувати альтернативи для їх надсилання (наприклад, фреймворки або бібліотеки).

Користувач, під яким працює веб-сервер, повинен бути доданий до списку довірених у конфігурації sendmail, щоб уникнути додавання заголовка 'X-Warning' при вказівці відправника за допомогою опції (-f). Для користувачів sendmail – це файл /etc/mail/trusted-users.

### Значення, що повертаються

Повертає **`true`**якщо лист був прийнятий для передачі, інакше **`false`**

Важливо зауважити, що те, що лист був прийнятий для передачі зовсім не означає, що він досяг одержувача.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `additional_headers` може набувати значення типу масив. |

### Приклади

**Приклад #1 Надсилання листа.**

Використання функції **mail()** для надсилання простого листа:

```php
<?php
// Сообщение
$message = "Line 1\r\nLine 2\r\nLine 3";

// На случай если какая-то строка письма длиннее 70 символов мы используем wordwrap()
$message = wordwrap($message, 70, "\r\n");

// Отправляем
mail('caffeinated@example.com', 'My Subject', $message);
?>
```

**Приклад #2 Надсилання листа з додатковими заголовками.**

Додавання простих заголовків, які повідомляють поштовому агенту адреси From та Reply-To:

```php
<?php
$to      = 'nobody@example.com';
$subject = 'the subject';
$message = 'hello';
$headers = 'From: webmaster@example.com' . "\r\n" .
    'Reply-To: webmaster@example.com' . "\r\n" .
    'X-Mailer: PHP/' . phpversion();

mail($to, $subject, $message, $headers);
?>
```

**Приклад #3 Надсилання листа з додатковими заголовками, переданими масивом**

У цьому прикладі надсилається той же лист, що і в прикладі вище, але додаткові заголовки задаються масивом (доступно з PHP 7.2.0).

```php
<?php
$to      = 'nobody@example.com';
$subject = 'the subject';
$message = 'hello';
$headers = array(
    'From' => 'webmaster@example.com',
    'Reply-To' => 'webmaster@example.com',
    'X-Mailer' => 'PHP/' . phpversion()
);

mail($to, $subject, $message, $headers);
?>
```

**Приклад #4 Надсилання листа з додатковими аргументами командного рядка.**

Параметр `additional_params` може бути використаний для передачі додаткових параметрів програмі, яка використовується для надсилання листів за допомогою директиви `sendmail_path`

```php
<?php
mail('nobody@example.com', 'the subject', 'the message', null,
   '-fwebmaster@example.com');
?>
```

**Приклад #5 Надсилання HTML-повідомлення**

За допомогою функції **mail()** також можна надіслати і HTML-лист.

```php
<?php
// несколько получателей
$to = 'johny@example.com, sally@example.com'; // обратите внимание на запятую

// тема письма
$subject = 'Birthday Reminders for August';

// текст письма
$message = '
<html>
<head>
  <title>Birthday Reminders for August</title>
</head>
<body>
  <p>Here are the birthdays upcoming in August!</p>
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

// Для отправки HTML-письма должен быть установлен заголовок Content-type
$headers  = 'MIME-Version: 1.0' . "\r\n";
$headers .= 'Content-type: text/html; charset=iso-8859-1' . "\r\n";

// Дополнительные заголовки
$headers[] = 'To: Mary <mary@example.com>, Kelly <kelly@example.com>';
$headers[] = 'From: Birthday Reminder <birthday@example.com>';
$headers[] = 'Cc: birthdayarchive@example.com';
$headers[] = 'Bcc: birthdaycheck@example.com';

// Отправляем
mail($to, $subject, $message, implode("\r\n", $headers));
?>
```

> **Зауваження**
> 
> Для надсилання HTML або інших комплексних повідомлень рекомендується використовувати PEAR-пакет [» PEAR::Mail\_Mime](https://pear.php.net/package/Mail_Mime)

### Примітки

> **Зауваження**
> 
> Реалізація SMTP (лише Windows) функції **mail()** У Windows багато в чому відрізняється від реалізації в sendmail. По-перше, вона не використовує локальну програму для складання листів, а працює безпосередньо з сокетами, що означає, що необхідний поштовий агент (`MTA`), що очікує з'єднань на сокеті (може бути як на локальному, так і на віддаленому сервері).
> 
> По-друге, додаткові заголовки на кшталт: `From:` `Cc:` `Bcc:` і `Date:` інтерпретуються насамперед *не* `MTA`, а PHP.
> 
> Тому параметр `to` не має бути адресою виду "Something [someone@example.com](mailto:someone@example.com)Команда mail може неправильно інтерпретувати цю адресу під час передачі даних MTA.

> **Зауваження**
> 
> Не слід використовувати функцію **mail()** для надсилання великої кількості листів у циклі. Функція відкриває та закриває з'єднання з SMTP-сервером для кожного листа, що не дуже ефективно.
> 
> Для надсилання великої кількості повідомлень зверніть увагу на пакети [» PEAR::Mail](https://pear.php.net/package/Mail) і [» PEAR::Mail\_Queue](https://pear.php.net/package/Mail_Queue)

> **Зауваження**
> 
> Корисні RFC: [» RFC 1896](http://www.faqs.org/rfcs/rfc1896) [» RFC 2045](http://www.faqs.org/rfcs/rfc2045) [» RFC 2046](http://www.faqs.org/rfcs/rfc2046) [» RFC 2047](http://www.faqs.org/rfcs/rfc2047) [» RFC 2048](http://www.faqs.org/rfcs/rfc2048) [» RFC 2049](http://www.faqs.org/rfcs/rfc2049) і [» RFC 2822](http://www.faqs.org/rfcs/rfc2822)

### Дивіться також

-   [mb\_send\_mail()](function.mb-send-mail.html) - Надсилання закодованого повідомлення
-   [imap\_mail()](function.imap-mail.html) - Надіслати email
-   [» PEAR::Mail](https://pear.php.net/package/Mail)
-   [» PEAR::Mail\_Mime](https://pear.php.net/package/Mail_Mime)