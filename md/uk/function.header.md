---
navigation:
  - function.header-remove.md: « header\_remove
  - function.headers-list.md: headers\_list »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: header
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# header

(PHP 4, PHP 5, PHP 7, PHP 8)

header — Надсилає необроблений (сирий) HTTP-заголовок

### Опис

```methodsynopsis
header(string $header, bool $replace = true, int $response_code = 0): void
```

Функцию**header()** викликають для надсилання HTTP-заголовка. У [» специфікації HTTP/1.1](http://www.faqs.org/rfcs/rfc2616) докладно описані HTTP-заголовки.

Помните, функцию**header()** дозволено викликати тільки якщо клієнту ще не були передані дані. Тобто вона повинна йти першою у висновку, перед її викликом не повинно бути HTML-тегів, порожніх рядків тощо. Іноді виникає помилка, коли при читанні коду файловими функціями на кшталт [include](function.include.md) або [require](function.require.md) у коді трапляються пробіли або порожні рядки, які виводяться до виклику функції **header()**. Ті самі проблеми можуть виникати, коли в одному файлі записані PHP-код та HTML-розмітка.

```php
<html>
<?php

/* Этот Приклад приведёт к ошибке. Обратите внимание
 * на тег вверху, который будет выведен до вызова функции header() */
header('Location: http://www.example.com/');
exit;

?>
```

### Список параметрів

`header`

Рядок заголовка.

Існує два виклики заголовка, які відрізняються від інших. Перший - заголовок, який починається з рядка`HTTP/`»(Регістр не важливий). Цей заголовок визначає код стану HTTP для відповіді. Наприклад, якщо веб-сервер Apache через директиву `ErrorDocument` налаштований на обробку запитів до неіснуючих файлів PHP-скриптом, то розробник, ймовірно, захоче переконатися, що скрипт генерує правильний код стану.

```php
<?php

// Приклад иллюстрирует передачу заголовка "HTTP/".
// Из альтернативных способов в типичных случаях выбирают этот:
// 1. header($_SERVER["SERVER_PROTOCOL"] . " 404 Not Found");
//    (чтобы переопределить сообщения о состоянии HTTP для клиентов, которые все еще работают по протоколу HTTP/1.0)
// 2. http_response_code(404); (для определить сообщение по умолчанию)
header("HTTP/1.1 404 Not Found");

?>
```

Інший відмінний вид заголовка - "Location:". Він відправляє заголовок назад у браузер, а також повертає браузеру код стану `REDIRECT` (302), якщо тільки код стану `201`или`3xx` не було встановлено.

```php
<?php

header("Location: http://www.example.com/"); /* Перенаправление браузера */

/* Убедиться, что код ниже не будет выполнен после перенаправления .*/
exit;

?>
```

`replace`

Необов'язковий параметр `replace` визначає, чи повинен заголовок замінити попередній аналогічний заголовок або додати друге заголовок того ж типу. За умовчанням він замінить заголовок, але якщо передати **`false`**, Як другий аргумент, можна примусово задати кілька однотипних заголовків. Наприклад:

```php
<?php

header('WWW-Authenticate: Negotiate');
header('WWW-Authenticate: NTLM', false);

?>
```

`response_code`

Примусово вказує код відповіді HTTP. Зверніть увагу, що цей параметр працює тільки тоді, коли рядок `header`не пуста.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо не вдалося запланувати надсилання заголовка, функція **header()** видає помилку рівня **`E_WARNING`**

### Приклади

**Приклад #1 Діалог завантаження**

Якщо потрібно запропонувати користувачеві зберегти дані, що пересилаються, наприклад згенерований PDF-файл, вказують заголовок [» Content-Disposition](http://www.faqs.org/rfcs/rfc2183), який підставляє ім'я файлу, що рекомендується, і змушує браузер показати діалог збереження.

```php
<?php

// Будем передавать PDF
header('Content-Type: application/pdf');

// Он будет называться downloaded.pdf
header('Content-Disposition: attachment; filename="downloaded.pdf"');

// Исходный PDF-файл original.pdf
readfile('original.pdf');

?>
```

**Приклад #2 Директиви для роботи з кешем**

PHP-скрипти часто генерують динамічний зміст, який не повинен кешувати браузер клієнта або проміжний кеш між сервером та клієнтським браузером. Проксі-сервери та браузери можуть примусово відключити кешування, передавши заголовки:

```php
<?php

header("Cache-Control: no-cache, must-revalidate"); // HTTP/1.1
header("Expires: Sat, 26 Jul 1997 05:00:00 GMT"); // Дата в прошлом

?>
```

> **Зауваження** :
> 
> Бувають ситуації, в яких браузер не кешуватиме сторінки, навіть якщо наведені заголовки не були передані. Користувачам доступні установки браузера, які змінюють поведінку кешування за замовчуванням. Надсилаючи наведені заголовки, розробник повинен перевизначити будь-які налаштування, які в інших випадках призводять до кешування виведення скрипту.
> 
> Крім того, через функцію [session\_cache\_limiter()](function.session-cache-limiter.md) та директиву `session.cache_limiter` можна автоматично створювати правильні заголовки, пов'язані з кешуванням під час роботи з сесіями.

**Приклад #3 Налаштування cookie**

функцією [setcookie()](function.setcookie.md) зручно встановлювати cookies. Щоб встановити cookie з атрибутами, які не підтримують функцію [setcookie()](function.setcookie.md), викликають функцію **header()**

Наприклад, наступний код встановлює cookie з атрибутом `Partitioned`

```php
<?php

header('Set-Cookie: name=value; Secure; Path=/; SameSite=None; Partitioned;');

?>
```

### Примітки

> **Зауваження** :
> 
> Доступ до заголовків та їх висновок здійснюватиметься лише у випадку, якщо у SAPI є їх підтримка.

> **Зауваження** :
> 
> Щоб уникнути цієї проблеми, можна буферизувати висновок скрипта. Тоді всі дані, що виводяться, буферизуватимуться на сервері, поки не буде дана явна команда на пересилання даних. Керувати буферизацією можна вручну - функціями [ob\_start()](function.ob-start.md) і [ob\_end\_flush()](function.ob-end-flush.md), або поставивши директиву `output_buffering` у конфігураційному файлі php.ini, або налаштувавши конфігурацію сервера належним чином.

> **Зауваження** :
> 
> Рядок заголовка HTTP-стану буде відправлений клієнту першим, незалежно від того, чи викликана функція **header()** першою чи ні. Статус можна перевизначити у будь-який час викликом функції **header()** з новим рядком стану, якщо HTTP-заголовки ще не були надіслані.

> **Зауваження** :
> 
> Специфікація HTTP/1.1 вимагає, щоб як аргумент заголовка [» Location:](http://tools.ietf.org/html/rfc7231#section-7.1.2) був вказаний абсолютний URI, який би включав схему, ім'я хоста та абсолютний шлях, хоча іноді клієнти можуть приймати і відносні URI. Абсолютний URI можна побудувати самому через елементи [$\_SERVER\['HTTP\_HOST'\]](reserved.variables.server.md) [$\_SERVER\['PHP\_SELF'\]](reserved.variables.server.md) або функцією [dirname()](function.dirname.md) :
> 
> ```php
> <?php
> 
> /* Перенаправлення браузера на іншу сторінку в тій же директорії, яка
> була запитана */
> $host = $_SERVER['HTTP_HOST'];
> $uri = rtrim(dirname($_SERVER['PHP_SELF']), '/\\');
> $extra = 'mypage.php';
> header("Location: http://$host$uri/$extra");
> exit;
> 
> ?>
> ```

> **Зауваження** :
> 
> Ідентифікатор сесії не буде передаватися разом із заголовком Location, навіть якщо увімкнено налаштування [session.use\_trans\_sid](session.configuration.md#ini.session.use-trans-sid). Його потрібно передавати вручну, використовуючи константу **`SID`**

### Дивіться також

-   [headers\_sent()](function.headers-sent.md) \- Перевіряє, чи були надіслані заголовки
-   [setcookie()](function.setcookie.md) \- Надсилає cookie
-   [http\_response\_code()](function.http-response-code.md) \- Отримує або встановлює код відповіді HTTP
-   [header\_remove()](function.header-remove.md) \- Видаляє раніше встановлені заголовки
-   [headers\_list()](function.headers-list.md) \- Повертає список переданих заголовків (або готових до відправлення)
-   Розділ документації[HTTP-автентифікації](features.http-auth.md)
