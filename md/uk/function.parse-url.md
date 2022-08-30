Розбирає URL та повертає його компоненти

-   [httpbuildquery](function.http-build-query.html)
    
-   [rawurldecode »](function.rawurldecode.html)
    
-   [PHP Manual](index.html)
    
-   [Функції URL](ref.url.html)
    
-   Розбирає URL та повертає його компоненти
    

# parseurl

(PHP 4, PHP 5, PHP 7, PHP 8)

parseurl — Розбирає URL та повертає його компоненти

### Опис

```methodsynopsis
parse_url(string $url, int $component = -1): int|string|array|null|false
```

Ця функція розбирає URL-адресу і повертає асоціативний масив, що містить всі компоненти URL, які в ньому присутні. Елементи масиву *не будуть* декодовані як URL-адреса.

Ця функція *не* призначена для перевірки на коректність даного URL, вона лише розбиває його на перелічені нижче частини. Часткові та неприпустимі URL також приймаються, **parseurl()** намагається зробити все можливе щоб розібрати їх коректно.

### Список параметрів

`url`

URL для аналізу.

`component`

Вкажіть одну з констант **`PHP_URL_SCHEME`** **`PHP_URL_HOST`** **`PHP_URL_PORT`** **`PHP_URL_USER`** **`PHP_URL_PASS`** **`PHP_URL_PATH`** **`PHP_URL_QUERY`** або **`PHP_URL_FRAGMENT`**, щоб отримати лише конкретний компонент URL у вигляді рядка (string). Винятком є ​​вказівка **`PHP_URL_PORT`**, в цьому випадку значення, що повертається буде типу int.

### Значення, що повертаються

При розборі значно некоректних URL-адрес **parseurl()** може повернути **`false`**

Якщо параметр `component` буде опущено, функція поверне асоціативний масив (array). У масиві буде принаймні один елемент. Можливі ключі у цьому масиві:

-   scheme - наприклад, http
-   host
-   port
-   user
-   pass
-   path
-   query – після знака питання `?`
-   fragment - після знаку ґрат `#`

Якщо параметр `component` визначено, функція **parseurl()** поверне рядок (string) (або число (int), у разі **`PHP_URL_PORT`**) замість масиву (array). Якщо запитаний компонент не існує в даній URL-адресі, буде повернено **`null`**. Починаючи з PHP 8.0.0, **parseurl()** розрізняє відсутні та порожні запити та фрагменти:

```
http://example.com/foo → query = null, fragment = null
http://example.com/foo? → query = "",   fragment = null
http://example.com/foo# → query = null, fragment = ""
http://example.com/foo?# → query = "",   fragment = ""
```

Раніше у всіх випадках запит та фрагмент були **`null`**

Зверніть увагу, що символи керування (дивіться [ctypecntrl()](function.ctype-cntrl.html)) у компонентах замінюються підкресленням (`_`

### список змін

| Версия | Описание                                                                |
|--------|-------------------------------------------------------------------------|
|        | **parseurl()** тепер розрізняє відсутні та порожні запити та фрагменти. |

### Приклади

**Приклад #1 Приклад використання **parseurl()****

```php
<?php
$url = 'http://username:password@hostname:9090/path?arg=value#anchor';

var_dump(parse_url($url));
var_dump(parse_url($url, PHP_URL_SCHEME));
var_dump(parse_url($url, PHP_URL_USER));
var_dump(parse_url($url, PHP_URL_PASS));
var_dump(parse_url($url, PHP_URL_HOST));
var_dump(parse_url($url, PHP_URL_PORT));
var_dump(parse_url($url, PHP_URL_PATH));
var_dump(parse_url($url, PHP_URL_QUERY));
var_dump(parse_url($url, PHP_URL_FRAGMENT));
?>
```

Результат виконання цього прикладу:

```
array(8) {
  ["scheme"]=>
  string(4) "http"
  ["host"]=>
  string(8) "hostname"
  ["port"]=>
  int(9090)
  ["user"]=>
  string(8) "username"
  ["pass"]=>
  string(8) "password"
  ["path"]=>
  string(5) "/path"
  ["query"]=>
  string(9) "arg=value"
  ["fragment"]=>
  string(6) "anchor"
}
string(4) "http"
string(8) "username"
string(8) "password"
string(8) "hostname"
int(9090)
string(5) "/path"
string(9) "arg=value"
string(6) "anchor"
```

**Приклад #2 Приклад використання **parseurl()** за відсутності протоколу**

```php
<?php
$url = '//www.example.com/path?googleguy=googley';

// До 5.4.7 в path выводилось "//www.example.com/path"
var_dump(parse_url($url));
?>
```

Результат виконання цього прикладу:

```
array(3) {
  ["host"]=>
  string(15) "www.example.com"
  ["path"]=>
  string(5) "/path"
  ["query"]=>
  string(17) "googleguy=googley"
}
```

### Примітки

**Застереження**

Функція може видати некоректні результати для відносних або недійсних URL-адрес і результати можуть навіть не відповідати загальному поведінці HTTP-клієнтів. Якщо потрібно проаналізувати URL-адреси з ненадійних вхідних даних, потрібна додаткова перевірка, наприклад, за допомогою [filtervar()](function.filter-var.html) з фільтром **`FILTER_VALIDATE_URL`**

> **Зауваження**
> 
> Ця функція призначена спеціально для аналізу URL-адрес, а не URI. Однак, щоб відповідати вимогам зворотної сумісності PHP, вона робить виняток для протоколу file://, у якій допускаються потрійні сліші (file:///...). Для іншого протоколу це неприпустимо.

### Дивіться також

-   [pathinfo()](function.pathinfo.html) - Повертає інформацію про шлях до файлу
-   [parsestr()](function.parse-str.html) - Розбирає рядок у змінні
-   [httpbuildquery()](function.http-build-query.html) - Генерує URL-кодований рядок запиту
-   [dirname()](function.dirname.html) - Повертає ім'я батьківського каталогу із зазначеного шляху
-   [basename()](function.basename.html) - Повертає останній компонент імені із зазначеного шляху
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)