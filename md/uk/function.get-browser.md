Повідомляє про можливості браузера користувача

-   [« exit](function.exit.html)
    
-   [haltcompiler »](function.halt-compiler.html)
    
-   [PHP Manual](index.html)
    
-   [Різні функції](ref.misc.html)
    
-   Повідомляє про можливості браузера користувача
    

# getbrowser

(PHP 4, PHP 5, PHP 7, PHP 8)

getbrowser — Повідомляє про можливості браузера користувача

### Опис

```methodsynopsis
get_browser(?string $user_agent = null, bool $return_array = false): object|array|false
```

Намагається визначити можливості браузера користувача, шукаючи інформацію про браузер у файлі browscap.ini.

### Список параметрів

`user_agent`

Аналізований рядок із User Agent. За промовчанням використовується значення HTTP User-Agent. Однак цей параметр можна пропустити для отримання додаткової інформації про браузер.

Параметр може бути пропущений, якщо його значення буде рівним **`null`**

`return_array`

Якщо дорівнює **`true`**, то функція поверне масив (array) замість об'єкта (object).

### Значення, що повертаються

Інформація повертається як об'єкта, чи вигляді масиву, що містить різні дані, наприклад, мажорну і мінорну версію браузера і рядок ID; значення з **`true`\*\*\*\*`false`** для таких функцій браузера, як фрейми, JavaScript, cookies і т.д.

Наявність `cookies` означає, що браузер має можливість прийому cookies, а не повідомляє про те, чи ввімкнув користувач можливість прийому cookies чи ні. Єдиним способом перевірки можливості браузера приймати cookies є встановлення cookie за допомогою [setcookie()](function.setcookie.html), оновлення сторінки та перевірка значення.

Повертає **`false`**, якщо неможливо отримати інформацію, наприклад, коли параметр конфігурації [browscap](misc.configuration.html#ini.browscap) у php.ini не було встановлено.

### Приклади

**Приклад #1 Виведення інформації про браузер користувача**

```php
<?php
echo $_SERVER['HTTP_USER_AGENT'] . "\n\n";

$browser = get_browser(null, true);
print_r($browser);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.7) Gecko/20040803 Firefox/0.9.3

Array
(
    [browser_name_regex] => ^mozilla/5\.0 (windows; .; windows nt 5\.1; .*rv:.*) gecko/.* firefox/0\.9.*$
    [browser_name_pattern] => Mozilla/5.0 (Windows; ?; Windows NT 5.1; *rv:*) Gecko/* Firefox/0.9*
    [parent] => Firefox 0.9
    [platform] => WinXP
    [browser] => Firefox
    [version] => 0.9
    [majorver] => 0
    [minorver] => 9
    [cssversion] => 2
    [frames] => 1
    [iframes] => 1
    [tables] => 1
    [cookies] => 1
    [backgroundsounds] =>
    [vbscript] =>
    [javascript] => 1
    [javaapplets] => 1
    [activexcontrols] =>
    [cdf] =>
    [aol] =>
    [beta] => 1
    [win16] =>
    [crawler] =>
    [stripper] =>
    [wap] =>
    [netclr] =>
)
```

### Примітки

> **Зауваження**
> 
> Для роботи цієї функції необхідно, щоб в установці [browscap](misc.configuration.html#ini.browscap) в налаштуваннях php.ini було встановлено коректний шлях до файлу browscap.ini у вашій системі.
> 
> browscap.ini не постачається з PHP, але ви можете останню його версію тут: [» phpbrowscap.ini](http://browscap.org/)
> 
> browscap.ini містить інформацію про більшість браузерів, що вимагає оновлень для підтримки його бази актуальної Формат файлу досить очевидний.