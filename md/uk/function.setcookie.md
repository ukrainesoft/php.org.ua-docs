---
navigation:
  - function.pfsockopen.md: « pfsockopen
  - function.setrawcookie.md: setrawcookie »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: setcookie
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# setcookie

(PHP 4, PHP 5, PHP 7, PHP 8)

setcookie — Надсилає cookie

### Опис

```methodsynopsis
setcookie(    string $name,    string $value = "",    int $expires_or_options = 0,    string $path = "",    string $domain = "",    bool $secure = false,    bool $httponly = false): bool
```

Альтернативна сигнатура доступна з PHP 7.3.0 (іменовані параметри не підтримуються):

```methodsynopsis
setcookie(string $name, string $value = "", array $options = []): bool
```

Функция**setcookie()** задає значення cookie, яке буде надіслано клієнту разом з іншими заголовками HTTP. Як і інші заголовки файл cookie повинен передаватися *до* того, як буде виведено будь-які інші дані скрипту (це обмеження протоколу). Для цього потрібно викликати функцію до іншого висновку, включаючи виведення тегів `<html>`и`<head>`, а також порожні рядки та символи пробілів.

После установки cookie к нему можно будет получить доступ через суперглобальную переменную[$\_COOKIE](reserved.variables.cookies.md) при наступному завантаженні сторінки. Значення cookie також може містити суперглобальна змінна [$\_REQUEST](reserved.variables.request.md)

### Список параметрів

Стандарт[» RFC 6265](http://www.faqs.org/rfcs/rfc6265) дає конкретні вказівки у тому, як потрібно інтерпретувати кожен із параметрів **setcookie()**

`name`

Назву cookie.

`value`

Значення cookie. Це значення буде збережено на клієнтському комп'ютері; не записуйте секретні дані в cookie. Значення, присвоєне cookie з ім'ям `name`, допустим,`'cookiename'`, будет доступно через[$\_COOKIE\['cookiename'\]](reserved.variables.cookies.md)

`expires_or_options`

Час закінчення терміну дії cookie. Це позначка часу Unix, тобто кількість секунд від початку епохи. Один із способів встановлення значення – додати кількість секунд до закінчення терміну дії cookie до результату виклику функції [time()](function.time.md). Наприклад, вираз `time() + 60 * 60 * 24 * 30` встановить термін дії cookie, який закінчиться за 30 днів. Інший варіант – викликати функцію [mktime()](function.mktime.md). Якщо поставити або пропустити аргумент, термін дії cookie закінчиться із закінченням сесії (при закритті браузера).

> **Зауваження** :
> 
> Можна помітити, що параметр `expires_or_options`принимает в качестве значения метку времени Unix, а хранит его в формате`Wdy, DD-Mon-YYYY HH:MM:SS GMT`, причина цього те, що PHP робить це перетворення автоматично.

`path`

Шлях на сервері, яким будуть доступні значення cookie. Якщо поставити `«/»`, cookie будуть доступні у всьому домені `domain`. Якщо поставити `«/foo/»`, cookie будуть доступні тільки з директорії `/foo/` та її піддиректорій (наприклад, `/foo/bar/`) домена`domain`. Значення за промовчанням - поточна директорія, в якій PHP встановлює cookie.

`domain`

Домен або піддомен, якому доступні cookie. Завдання піддомену (наприклад, `«www.example.com»`) зробить cookie доступними в ньому та у всіх піддоменах (наприклад, w2.[www.example.com](http://www.example.com)). Щоб зробити cookie доступними для всього домену, включаючи піддомени, потрібно просто вказати ім'я домену (тобто `«example.com»`

Старі браузери, що йдуть застарілому стандарту [» RFC 2109](http://www.faqs.org/rfcs/rfc2109), можуть вимагати перед доменом, щоб умикалися всі піддомени.

`secure`

Вказує на те, що значення cookie має передаватися від клієнта із захищеного з'єднання HTTPS. Якщо поставлено **`true`**, cookie від клієнта буде передано на сервер, лише якщо встановлено захищене з'єднання. При передачі cookie від сервера клієнту програміст веб-сервера повинен стежити за тим, щоб cookie цього типу передавалися по захищеному каналу (наприклад, з урахуванням суперглобальної змінної) [$\_SERVER\["HTTPS"\]](reserved.variables.server.md)

`httponly`

Якщо поставлено **`true`**, cookie будуть доступні лише через протокол HTTP. Тобто cookie не будуть доступні скриптовим мовам на кшталт JavaScript. Було висловлено припущення, що цей параметр може ефективно зменшити крадіжку особистих даних через XSS-атаку (хоча він підтримується не всіма браузерами), але це твердження часто оспорюється. Може приймати значення **`true`** або **`false`**

`options`

Асоціативний масив (array), який може містити будь-який із ключів: `expires` `path` `domain` `secure` `httponly`и`samesite`. Якщо в масиві виявиться інший ключ, буде видано помилку рівня **`E_WARNING`**. Значення мають той самий сенс, який описаний для параметрів з тим самим ім'ям. Значення елемента `samesite` повинно бути або `None`, либо`Lax`или`Strict`. Якщо якась із дозволених опцій не вказана, її значення за умовчанням збігаються зі значеннями за промовчанням явних параметрів. Якщо елемент `samesite`не указан, функция не установит cookie-атрибут SameSite.

> **Зауваження** :
> 
> To set a cookie that includes attributes that aren't among the keys listed, use [header()](function.header.md)

### Значення, що повертаються

Якщо перед викликом функції клієнту вже передавався будь-який висновок (теги, порожні рядки, пробіли, текст тощо), **setcookie()** зазнає невдачі і поверне **`false`**. Якщо **setcookie()** успішно відпрацює, то поверне **`true`**. Це, однак, не означає, що клієнтська програма (браузер) правильно прийняла та обробила cookie.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Формат дати надісланих cookie тепер `«D, d M Y H:i:s \G\M\T»`; раніше він був `«D, d-M-Y H:i:s T»` |
| 7.3.0 | Додано альтернативний підпис, що підтримує масив опцій `options`. . Цей підпис також підтримує налаштування cookie-атрибута SameSite. |

### Приклади

Наступні приклади ілюструють низку способів відправлення cookies.

**Приклад #1 Приклад використання** setcookie()\*\*\*\*

```php
<?php

$value = 'что-то откуда-то';

setcookie("TestCookie", $value);
setcookie("TestCookie", $value, time()+3600);  /* срок действия 1 час */
setcookie("TestCookie", $value, time()+3600, "/~rasmus/", "example.com", 1);

?>
```

Варто зазначити, що значення cookie перед надсиланням клієнту піддається URL-коду. При зворотному отриманні значення cookie декодується і поміщається в змінну, з тим самим ім'ям, що ім'я cookie. Якщо ви не бажаєте, щоб значення кодувалися, використовуйте функцію [setrawcookie()](function.setrawcookie.md). Подивитися вміст наших тестових cookie можна, запустивши один із таких прикладів:

```php
<?php
// Вывести одно конкретное значение cookie
echo $_COOKIE["TestCookie"];

// В целях тестирования и отладки может пригодиться вывод всех cookie
print_r($_COOKIE);
?>
```

**Приклад #2 Приклад удаления cookie посредством**setcookie()\*\*\*\*

Щоб видалити cookie, достатньо як термін дії вказати якийсь час у минулому. Це запустить механізм браузера, що видаляє cookie, що минув. У нижченаведених прикладах показано, як видалити cookie, задані в попередніх прикладах:

```php
<?php
// установка даты истечения срока действия на час назад
setcookie("TestCookie", "", time() - 3600);
setcookie("TestCookie", "", time() - 3600, "/~rasmus/", "example.com", 1);
?>
```

**Приклад #3**setcookie()\*\* та масиви\*\*

Є можливість розміщувати в cookie масиви. Для цього кожному cookie потрібно дати ім'я відповідно до правил іменування масивів. Така можливість дозволяє помістити стільки значень, скільки є елементів у масиві. При зворотному отриманні всі ці значення будуть поміщені в масив з ім'ям цього cookie:

```php
<?php
// отправка cookie
setcookie("cookie[three]", "cookiethree");
setcookie("cookie[two]", "cookietwo");
setcookie("cookie[one]", "cookieone");

// после перезагрузки страницы, выведем cookie
if (isset($_COOKIE['cookie'])) {
    foreach ($_COOKIE['cookie'] as $name => $value) {
        $name = htmlspecialchars($name);
        $value = htmlspecialchars($value);
        echo "$name : $value <br />\n";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
three : cookiethree
two : cookietwo
one : cookieone
```

> **Зауваження**: Вказівка ​​символів-розділювачів на кшталт `[`и`]` у складі імені cookie не відповідає 4-му розділу стандарту RFC 6265, але має підтримуватися агентами користувача, як зазначено у розділі 5 стандарту RFC 6265.

### Примітки

> **Зауваження** :
> 
> Дозволено буферизувати висновок для надсилання виводу до виклику цієї функції, при цьому виведення в браузер буферизується на сервері доти, доки не буде відправлений. Це роблять викликом у скрипті функцій [ob\_start()](function.ob-start.md) і [ob\_end\_flush()](function.ob-end-flush.md), або включають директиву конфігурації `output_buffering` у файлі php.ini або файлах конфігурації сервера.

Загальні зауваження:

-   Cookie стануть видимими лише після перезавантаження сторінки, для якої вони мають бути помітні. Для перевірки, чи правильно встановлені cookie, їх перевіряють при наступному завантаженні сторінки до закінчення терміну дії. Термін дії cookie задають у параметрі`expires_or_options`. Хороший спосіб налагодити наявність файлів cookie - просто викликати функцію`print_r($_COOKIE);`
-   При видаленні cookie повинні бути задані самі параметри, що і при установці. Якщо в якості значення встановити пустий рядок, а інші параметри відповідають попередньому виклику функції setcookie, то cookie з заданим ім'ям буде видалено на віддаленому клієнті. Внутрішньо це виглядає так: cookie буде надано значення`«deleted»`, а термін дії переноситься на рік у минуле.
-   Оскільки встановлення значення\*\*`false`**призведе до видалення cookie, не потрібно задавати cookie логічні значення. Натомість можна вказати для**`false`**и для**`true`\*\*
-   Імена cookie дозволено встановлювати масивом імен, які будуть доступні в PHP-скрипті як масиви, але в системі користувача вони зберігатимуться у вигляді окремих записів. Для завдання cookie з кількома іменами та значеннями рекомендовано викликати функцію[explode()](function.explode.md). Не рекомендовано користуватися для цього функцією[serialize()](function.serialize.md)оскільки це порушує безпеку.

Численні виклики функції **setcookie()** виконуються у порядку дзвінка.

### Дивіться також

-   [header()](function.header.md) \- Надсилає необроблений (сирий) HTTP-заголовок
-   [setrawcookie()](function.setrawcookie.md) \- Надсилає cookie без URL-кодування значення
-   [розділ cookies](features.cookies.md)
-   [» RFC 6265](http://www.faqs.org/rfcs/rfc6265)
-   [» RFC 2109](http://www.faqs.org/rfcs/rfc2109)
