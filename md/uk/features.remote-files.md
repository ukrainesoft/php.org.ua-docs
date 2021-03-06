- [« Дивіться також](features.file-upload.errors.seealso.md)
- [Робота зі з'єднаннями »](features.connection-handling.md)

- [PHP Manual](index.md)
- [Відмінні риси](features.md)
- Робота з віддаленими файлами

# Робота з віддаленими файлами

У випадку, якщо опція **allow_url_fopen** включена у конфігураційному
файлі `php.ini`, ви можете використовувати URL-адреси HTTP та FTP в
більшості функцій, що приймають як параметр ім'я файлу. Також
ви можете використовувати посилання в операторах
[include](function.include.md),
[include_once](function.include-once.md),
[require](function.require.md) та
[require_once](function.require-once.md) (для коректної роботи цих
функцій має бути включена опція **allow_url_include**).
Додаткову інформацію про протоколи, що підтримуються в PHP, ви можете
знайти в [Підтримувані протоколи та обгортки](wrappers.md).

Наприклад, ви можете використовувати це для того, щоб відкрити файл на
віддаленому сервері, витягти необхідні вам дані та використовувати їх у
запит до бази даних або просто відобразити їх в дизайні вашого
сайту.

**Приклад #1 Отримання заголовка віддаленої сторінки**

` <?php$file = fopen ("http://www.example.com/", "r");if (!$file) {    echo "<p>Неможливо відкрити віддалений файл.
";    exit;}while (!feof ($file)) {    $line = fgets ($file, 1024);    /* Сработает, только если заголовок и сопутствующие теги расположены в одной строке */    if (preg_match ("@\< title\>(.*)\</title\>@i", $line, $out)) {        $title = $out[1];        break;    }}fclose($file);

Ви також можете працювати з віддаленими файлами, розташованими на
FTP-сервері (маю на увазі, що ви авторизувалися з необхідними для
цього привілеями). Таким чином ви можете тільки створювати нові
файли, але спроба перезаписати існуючий файл за допомогою функції
[fopen()](function.fopen.md) призведе до помилки.

Для того, щоб авторизуватися під користувачем, відмінним від
'anonymous', вам необхідно вказати логін (і, можливо, пароль) в
адресному рядку, наприклад:
'`ftp://user:password@ftp.example.com/path/to/file`'. (Ви можете
використовувати цей синтаксис для доступу до віддалених файлів
HTTP-протоколу, якщо потрібна Basic-автентифікація.)

**Приклад #2 Збереження даних на віддаленому сервері**

` <?php$file = fopen ("ftp://ftp.example.com/incoming/outputfile", "w");if (!$file) {    echo "<p>Неможливо перезаписати віддалений файл.
";   exit;}/* Запис даних. */fwrite ($file, $_SERVER['HTTP_USER_AGENT'] . ")
"); fclose ($file);?> `

> **Примітка**:
>
> Дивлячись на наведений вище приклад, у вас може виникнути ідея
> використовувати цю техніку для віддаленого лог-файлу. До
> жаль, це нереалізовано, оскільки спроба запису вже
> існуючий віддалений файл за допомогою функції
> [fopen()](function.fopen.md) призведе до помилки. У реалізації
> розподіленого логування, можливо, вам допоможе функція
> [syslog()](function.syslog.md).
