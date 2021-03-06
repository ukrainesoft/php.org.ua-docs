- [« header_remove](function.header-remove.md)
- [headers_list »](function.headers-list.md)

- [PHP Manual](index.md)
- [Мережні функції](ref.network.md)
- Надсилання HTTP-заголовка

# header

(PHP 4, PHP 5, PHP 7, PHP 8)

header — Надсилання HTTP-заголовка

### Опис

**header**(string `$header`, bool `$replace` = **`true`**, int
`$response_code` = 0): void

**header()** використовується для надсилання заголовка HTTP. У [» специфікації HTTP/1.1](http://www.faqs.org/rfcs/rfc2616) є докладний опис
HTTP-заголовки.

Пам'ятайте, що функцію **header()** можна викликати лише якщо клієнту ще
не передавалися дані. Тобто вона має йти першою у висновку, перед
її викликом має бути ніяких HTML-тегів, порожніх рядків тощо.
Досить часто виникає помилка, коли при читанні файлового коду
функціями, на кшталт [include](function.include.md) або
[require](function.require.md), у цьому коді трапляються пробіли або
порожні рядки, які відображаються до виклику **header()**. Ті ж проблеми
можуть виникати при використанні PHP/HTML в одному файлі.

`<html><?php/* Цей приклад приведе до помилки. Зверніть увагу на тег вгорі, який буде виведений до виклику header()

### Список параметрів

`header`
Рядок заголовка.

Існує два спеціальні заголовки. Один з них починається з "HTTP/"
(реєстр не важливий) і використовується для надсилання коду стану HTTP.
Наприклад, якщо веб-сервер Apache налаштований таким чином, щоб
запити до неіснуючих файлів оброблялися засобами PHP-скрипту
(використовуючи директиву `ErrorDocument`), ви напевно захочете переконатися,
що скрипт генерує правильний код стану.

`<?php// Цей приклад ілюструє особий випадок "HTTP/".// Кращі альтернативи в типових випадках використання включають://1. header($_SERVER["SERVER_PRO    щоб перевизначити повідомлення про стан http для клієнтів, все ще використовують HTTP/1.0)// 2. http_response_code(404); (для використання повідомлення за умовчанням)header("HTTP/1.1 404 Not Found");?> `

Іншим спеціальним видом заголовків є "Location:". В цьому випадку
функція не тільки надсилає цей заголовок браузеру, але також
повертає йому код стану `REDIRECT` (302), якщо раніше не був
встановлений код `201` або `3xx`.

`<?phpheader("Location: http://www.example.com/"); /* Перенаправлення браузера *//* Переконатися, код нижче не виконається після перенаправлення .*/exit;?> `

`replace`
Необов'язковий параметр `replace` визначає, чи треба замінювати
попередній аналогічний заголовок або заголовок того самого типу. за
замовчуванням заголовок буде замінено, але якщо передати **`false`**, можна
встановити кілька однотипних заголовків. Наприклад:

` <?phpheader('WWW-Authenticate: Negotiate');header('WWW-Authenticate: NTLM', false);?> `

`response_code`
Примусово визначає код відповіді HTTP. Слід враховувати, що це буде
працювати, тільки якщо рядок `header` не є порожнім.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо не вдалося запланувати надсилання заголовка, **header()** видає
помилку рівня **`E_WARNING`**.

### Приклади

**Приклад #1 Діалог завантаження**

Якщо необхідно попередити користувача про необхідність зберегти
дані, що пересилаються, такі як згенерований PDF-файл, можна
скористатися заголовком
[» Content-Disposition](http://www.faqs.org/rfcs/rfc2183), який
підставляє рекомендоване ім'я файлу та змушує браузер показати діалог
завантаження.

` <?php// Передаватимемо PDFheader('Content-Type: application/pdf');// Він називатися downloaded.pdfheader('Content-Disposition: attachment; filename="downloaded.pdf"');// PDF-файл original.pdfreadfile('original.pdf');?> `

**Приклад #2 Директиви для роботи з кешем**

PHP-скрипти часто генерують динамічний контент, який не повинен
кешуватися клієнтським браузером або будь-якими проміжними
обробниками, на зразок проксі-серверів. Можна примусово вимкнути
кешування на багатьох проксі-серверах та браузерах, передавши заголовки:

`<?phpheader("Cache-Control: no-cache, must-revalidate"); // HTTP/1.1header("Expires: Sat, 26 Jul 1997 05:00:00 GMT"); // Дата в минулому?> `

> **Примітка**:
>
> У деяких випадках ваші сторінки не кешуватимуться браузером,
> навіть якщо ви не передавали ці заголовки. У браузерах є
> певні установки, за допомогою яких користувач може змінювати
> Звичайний хід кешування, відключати його. Ви повинні перевизначати будь-які
> налаштування, які можуть вплинути на кешування скрипта, надсилаючи
> наведені вище заголовки.
>
> Крім того, для випадків, коли використовуються сесії, можна задати
> Налаштування конфігурації
> [session_cache_limiter()](function.session-cache-limiter.md) та
> `session.cache_limiter`. Ці установки можна використовувати для
> автоматичної генерації заголовків управляючих кешуванням.

### Примітки

> **Примітка**:
>
> Доступ до заголовків та їх виведення здійснюватиметься лише у випадку,
> якщо у SAPI є їх підтримка.

> **Примітка**:
>
> Щоб уникнути цієї проблеми, можна буферизувати висновок скрипта. В цьому
> у випадку всі виведені дані буферизуватимуться на сервері, поки не
> буде дана явна команда на пересилання даних. Керувати буферизацією
> можна вручну функціями [ob_start()](function.ob-start.md) та
> [ob_end_flush()](function.ob-end-flush.md) або задавши директиву
> `output_buffering` у конфігураційному файлі `php.ini`, або ж настроївши
> відповідним чином конфігурацію сервера.

> **Примітка**:
>
> Рядок заголовка стану HTTP завжди надсилатиметься клієнту
> першою, незалежно від цього був відповідний виклик функції
> **header()** першим чи ні. Цей стан можна перезаписати, викликаючи
> **header()** з новим рядком стану у будь-який час, коли можна
> надсилати HTTP-заголовки.

> **Примітка**:
>
> Специфікація HTTP/1.1 вимагає вказувати абсолютний URI як
> аргументу
> [» Location:](http://tools.ietf.org/html/rfc7231#section-7.1.2),
> включає схему, ім'я хоста та абсолютний шлях, хоча деякі клієнти
> здатні приймати та відносні URI. Абсолютний URI можна побудувати
> самостійно за допомогою `$_SERVER['HTTP_HOST']`,
> `$_SERVER['PHP_SELF']` та [dirname()](function.dirname.md):
>
> ` <?php/* Перенаправлення браузера на іншу сторінку в тією ж директорії, ізначально запитана */$host  = $_SERVER['HTTP_HOST'];$uri     | /\');$extra = 'mypage.php';header("Location: http://$host$uri/$extra");exit;?> `

> **Примітка**:
>
> Ідентифікатор сесії не передаватиметься разом із заголовком
> Location, навіть якщо увімкнено налаштування
> [session.use_trans_sid](session.configuration.md#ini.session.use-trans-sid).
> Його потрібно передавати вручну, використовуючи константу **`SID`**.

### Дивіться також

- [headers_sent()](function.headers-sent.md) - Перевіряє, чи були вони
надіслано заголовки
- [setcookie()](function.setcookie.md) - Надсилає cookie
- [http_response_code()](function.http-response-code.md) - Отримує
або встановлює код відповіді HTTP
- [header_remove()](function.header-remove.md) - Видаляє раніше
встановлені заголовки
- **header_list()**
- Розділ документації [HTTP-аутентифікації](features.http-auth.md)
