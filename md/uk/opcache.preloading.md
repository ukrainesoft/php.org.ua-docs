Preloading

-   [« Типы ресурсов](opcache.resources.html)
    
-   [Функции OPcache »](ref.opcache.html)
    
-   [PHP Manual](index.html)
    
-   [OPcache](book.opcache.html)
    
-   Preloading
    

# Preloading

Починаючи з PHP 7.4.0, можна налаштувати завантаження скриптів в opcache в момент старту PHP. Будь-які функції, класи, інтерфейси або трейти (але не константи) у цих файлах будуть глобально доступні для всіх запитів без їх явного завантаження. Таке передзавантаження дозволяє досягти більших зручностей і продуктивності (бо код завжди доступний) за рахунок використання більшої кількості пам'яті. Також, при внесенні змін у завантажені скрипти, щоб ці зміни стали доступними, доведеться перезавантажити PHP. З цього випливає, що передзавантаження має сенс використовувати лише у промисловому оточенні, але не в розробницькому.

Зверніть увагу, що баланс підвищення продуктивності та споживання пам'яті залежить від вашої програми. "Предзавантаження всього на світі" може бути найпростішою стратегією, але зовсім не обов'язково кращою. Також, передзавантаження працюватиме лише у випадку, коли PHP працює в режимі обслуговування запитів без перезавантаження. Таким чином, хоч передзавантаження можна використовувати в режимі CLI з включеним opcache, але, в більшості випадків безглуздо. Винятком є ​​використання передзавантаження з [библиотеками FFI](ffi.examples-complete.html)

> **Зауваження**
> 
> Завантаження не підтримується у Windows.

Налаштування передзавантаження складається з двох етапів і вимагає ввімкненого opcache. Для початку, налаштуйте [opcache.preload](opcache.configuration.html#ini.opcache.preload) у php.ini:

opcache.preload=preload.php

preload.php - це обов'язковий файл, який запуститься один раз при старті сервера (PHP-FPM, modphp, etc.) і який завантажить код на постійну пам'ять. Якщо PHP буде запущено під користувачем root (не рекомендується), значення [opcache.preload\_user](opcache.configuration.html#ini.opcache.preload-user) повинно містити ім'я користувача для запуску передзавантаження. Запуск завантаження під користувачем root заборонено.

У скрипті preload.php, будь-який файл вказаний у [include](function.include.html) [include\_once](function.include-once.html) [require](function.require.html) [require\_once](function.require-once.html) або [opcache\_compile\_file()](function.opcache-compile-file.html) буде завантажено на постійну пам'ять. У наступному прикладі будуть завантажені всі файли .php в директорії src, якщо вони не містять `Test` у імені.

```php
<?php
$directory = new RecursiveDirectoryIterator(__DIR__ . '/src');
$fullTree = new RecursiveIteratorIterator($directory);
$phpFiles = new RegexIterator($fullTree, '/.+((?<!Test)+\.php$)/i', RecursiveRegexIterator::GET_MATCH);

foreach ($phpFiles as $key => $file) {
    require_once($file[0]);
}
?>
```

І [include](function.include.html) і [opcache\_compile\_file()](function.opcache-compile-file.html) будуть працювати, але при цьому будуть трохи по-різному оброблені.

-   [include](function.include.html) запустить код із файлу, а [opcache\_compile\_file()](function.opcache-compile-file.html) ні. Це вплине лише на умовні декларації (функції, оголошені в блоках if).
-   Через те що [include](function.include.html) запустить код, вкладені [include](function.include.html) також будуть оброблені та передзавантажені.
-   [opcache\_compile\_file()](function.opcache-compile-file.html) може завантажувати файли у будь-якому порядку. Тобто якщо файл a.php визначає клас `A` та b.php визначає клас `B`, який є спадкоємцем `A`, то [opcache\_compile\_file()](function.opcache-compile-file.html) може завантажити ці два файли у будь-якому порядку. При використанні [include](function.include.html), з іншого боку, a.php *повинен бути* завантажений першим.
-   У будь-якому випадку, якщо якийсь скрипт надалі запросить включення вже завантаженого скрипта, то він буде виконаний, але сутності перетворюватися не будуть. Використання [include\_once](function.include-once.html) не запобігає повторному увімкненню файлу. Може знадобитися завантажити файл знову, щоб увімкнути певні глобальні константи, оскільки вони не обробляються попереднім завантаженням.

Який підхід використовувати – залежить від бажаної поведінки. Для коду, який використовує автозавантажувач, підхід [opcache\_compile\_file()](function.opcache-compile-file.html) дасть більше гнучкості. З кодом, який завантажуватиметься вручну, варіант з [include](function.include.html) може бути надійнішим.