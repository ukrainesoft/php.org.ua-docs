---
navigation:
  - features.commandline.interactive.md: « Інтерактивна консоль
  - features.commandline.ini.md: Опції конфігурації »
  - index.md: PHP Manual
  - features.commandline.md: Робота з PHP з командного рядка
title: Вбудований веб-сервер
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вбудований веб-сервер

**Увага**

Веб-сервер призначений для допомоги у розробці програм. Він також може бути корисним у тестових цілях або для демонстрації програми, що запускається у повністю контрольованому оточенні. Він не виконує повноцінного веб-сервера і не повинен використовуватися в загальнодоступних мережах.

Модуль CLI SAPI містить вбудований веб-сервер.

Веб-сервер виконує лише один однопотоковий процес, тому програми PHP зупинятимуться, якщо запит заблокований.

URI запити обслуговуються з поточної директорії, в якій було запущено PHP, якщо не використовується опція -t для явного вказівки кореневого документа. Якщо URI запиту не вказує на певний файл, то буде повернутий index.php або index.md у вказаній директорії. Якщо жоден із файлів не існує, то пошук цих файлів буде продовжено в батьківській директорії і так далі, доки вони не будуть знайдені або було досягнуто коріння документа. Якщо знайдено index.php або index.md, він повертається, а в $\_SERVER\['PATH\_INFO'\] буде знайдено останню частину URL-адреси. В іншому випадку повертається код відповіді 404.

Якщо PHP-файл вказується в командному рядку, коли запускається веб-сервер, він розглядається як скрипт "маршрутизації" (router). Скрипт виконується на початку кожного HTTP-запиту. Якщо цей скрипт повертає **`false`**, То запитуваний ресурс повертається як є. В іншому випадку браузеру буде повернено виведення цього скрипту.

Стандартні MIME-типи повертаються для файлів з такими розширеннями: .3gp, .apk, .avi, .bmp, .css, .csv, .doc, .docx, .flac, .gif, .gz, .gzip, .htm, .md, .ics, .jpe, .jpeg, .jpg, .js, .kml, .kmz, .m4a, .mov, .mp3, .mp4, .mpeg, .mpg, .odp, .ods, .odt , .oga, .ogg, .ogv, .pdf, .pdf, .png, .pps, .pptx, .qt, .svg, .swf, .tar, .text, .tif, .txt, .wav, . webm, .wmv, .xls, .xlsx, .xml, .xsl, .xsd та .zip.

**Історія правок: Підтримувані MIME-типи (розширення файлів)**

| Версия | Опис |
| --- | --- |
| 5.5.12 | .xml, .xsl, та .xsd |
| 5.5.7 | .3gp, .apk, .avi, .bmp, .csv, .doc, .docx, .flac, .gz, .gzip, .ics, .kml, .kmz, .m4a, .mp3, .mp4, .mpg , .mpeg, .mov, .odp, .ods, .odt, .oga, .pdf, .pptx, .pps, .qt, .swf, .tar, .text, .tif, .wav, .wmv, . xls, .xlsx та .zip |
| 5.5.5 | .pdf |
| 5.4.11 | .ogg, .ogv, та .webm |
| 5.4.4 | .htm та .svg |

**Історія змін**

| Версия | Опис |
| --- | --- |
| 7.4.0 | Ви можете налаштувати вбудований веб-сервер так, щоб він виконував розгалуження кількох воркерів для перевірки коду, який потребує кількох одночасних запитів до вбудованого веб-сервера. Задайте у змінній оточення PHP\_CLI\_SERVER\_WORKERS кількість необхідних воркерів перед запуском сервера. Не підтримується у Windows. |
| **Увага** |  |

Ця *експериментальна*функция*не* призначена для продакшен використання. Зазвичай вбудований веб-сервер *не*предназначен для продакшен использования.

**Приклад #1 Запуск веб-сервера**

$ cd ~/public\_html $ php -S localhost:8000

У консолі виведеться:

```
PHP 5.4.0 Development Server started at Thu Jul 21 10:43:28 2011
Listening on localhost:8000
Document root is /home/me/public_html
Press Ctrl-C to quit
```

Після URI-запитів [http://localhost:8000/](http://localhost:8000/) і [http://localhost:8000/myscript.md](http://localhost:8000/myscript.md) в консолі виведеться приблизно таке:

```
PHP 5.4.0 Development Server started at Thu Jul 21 10:43:28 2011
Listening on localhost:8000
Document root is /home/me/public_html
Press Ctrl-C to quit.
[Thu Jul 21 10:48:48 2011] ::1:39144 GET /favicon.ico - Request read
[Thu Jul 21 10:48:50 2011] ::1:39146 GET / - Request read
[Thu Jul 21 10:48:50 2011] ::1:39147 GET /favicon.ico - Request read
[Thu Jul 21 10:48:52 2011] ::1:39148 GET /myscript.md - Request read
[Thu Jul 21 10:48:52 2011] ::1:39149 GET /favicon.ico - Request read
```

Зверніть увагу, що до PHP 7.4.0 статичні ресурси із символічними посиланнями не були доступні у Windows, якщо тільки скрипт маршрутизатора не обробив би їх.

**Приклад #2 Запуск із зазначенням кореневої директорії**

$ cd ~/public\_html $ php -S localhost:8000 -t foo/

У консолі виведеться:

```
PHP 5.4.0 Development Server started at Thu Jul 21 10:50:26 2011
Listening on localhost:8000
Document root is /home/me/public_html/foo
Press Ctrl-C to quit
```

**Приклад #3 Використання скрипта маршрутизації**

У цьому прикладі запити зображень будуть відображати їх, але запити HTML-файлів будуть повертати "Ласкаво просимо до PHP".

```php
<?php
// router.php
if (preg_match('/\.(?:png|jpg|jpeg|gif)$/', $_SERVER["REQUEST_URI"])) {
    return false;    // сервер возвращает файлы напрямую.
} else {
    echo "<p>Добро пожаловать в PHP</p>";
}
?>
```

$ php -S localhost:8000 router.php

**Увага**

Вбудований веб-сервер не повинен використовуватись у загальнодоступній мережі.

**Приклад #4 Перевірка використання веб-сервера CLI**

Для спільного використання скрипта маршрутизації при розробці з веб-сервером CLI і надалі з робочим веб-сервером:

```php
<?php
// router.php
if (php_sapi_name() == 'cli-server') {
    /* Маршрутизация с заданными правилами и возврат false */
}
/* продолжение с обычными операциями index.php */
?>
```

$ php -S localhost:8000 router.php

**Приклад #5 Підтримка типів файлів, що не підтримуються.**

Якщо вам потрібно обслуговувати статичні ресурси з MIME-типами, які не підтримує веб-сервер CLI, використовуйте це:

```php
<?php
// router.php
$path = pathinfo($_SERVER["SCRIPT_FILENAME"]);
if ($path["extension"] == "el") {
    header("Content-Type: text/x-script.elisp");
    readfile($_SERVER["SCRIPT_FILENAME"]);
}
else {
    return FALSE;
}
?>
```

$ php -S localhost:8000 router.php

**Приклад #6 Доступ до веб-сервера CLI з віддалених машин**

Ви можете зробити веб-сервер доступним на 8000 портах для всіх мережевих інтерфейсів:

$ php -S 0.0.0.0:8000
