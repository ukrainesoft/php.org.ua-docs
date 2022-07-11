- [«http_build_query](function.http-build-query.md)
- [rawurldecode »](function.rawurldecode.md)

- [PHP Manual](index.md)
- [Функції URL](ref.url.md)
- Розбирає URL та повертає його компоненти

#parse_url

(PHP 4, PHP 5, PHP 7, PHP 8)

parse_url — Розбирає URL та повертає його компоненти

### Опис

**parse_url**(string `$url`, int `$component` = -1):
int\|string\|array\|null\|false

Ця функція розбирає URL та повертає асоціативний масив, що містить
всі компоненти URL, які у ньому присутні. Елементи масиву *не
будуть декодовані як URL.

Ця функція *не* призначена для перевірки на правильність даного URL,
вона тільки розбиває його на перелічені нижче частини. Часткові та
неприпустимі URL також приймаються, **parse_url()** намагається зробити все
можливе, щоб розібрати їх коректно.

### Список параметрів

`url`
URL для аналізу.



`component`
Вкажіть одну з констант **`PHP_URL_SCHEME`**, **`PHP_URL_HOST`**,
**`PHP_URL_PORT`**, **`PHP_URL_USER`**, **`PHP_URL_PASS`**,
**`PHP_URL_PATH`**, **`PHP_URL_QUERY`** або **`PHP_URL_FRAGMENT`**,
щоб отримати лише конкретний компонент URL у вигляді рядка (string).
Винятком є вказівка **`PHP_URL_PORT`**, у цьому випадку
значення, що повертається буде типу int.

### Значення, що повертаються

При розборі значно некоректних URL-адрес **parse_url()** може
повернути **`false`**.

Якщо параметр `component` буде опущений, функція поверне асоціативний
масив (array). У масиві перебуватиме принаймні один елемент.
Можливі ключі у цьому масиві:

- `scheme` - наприклад, http
- `host`
- `port`
- `user`
- `pass`
- `path`
- `query` - після знаку питання `?`
- `fragment` - після знаку ґрати `#`

Якщо параметр `component` визначено, функція **parse_url()** поверне
рядок (string) (або число (int), у разі **`PHP_URL_PORT`**) замість
масиву (array). Якщо запитаний компонент не існує у цьому URL-адресі,
буде повернено **`null`**. Починаючи з PHP 8.0.0, parse_url()**
розрізняє відсутні та порожні запити та фрагменти:

http://example.com/foo → query = null, fragment = null
http://example.com/foo? → query = "", fragment = null
http://example.com/foo# → query = null, fragment = ""
http://example.com/foo?# → query = "", fragment = ""

Раніше у всіх випадках запит та фрагмент були **`null`**.

Зверніть увагу, що керуючі символи (дивіться
[ctype_cntrl()](function.ctype-cntrl.md)) у компонентах замінюються
підкресленням (`_`).

### Список змін

| Версія | Опис                                                                     |
| ------ | ------------------------------------------------------------------------ |
| 8.0.0  | **parse_url()** тепер розрізняє відсутні та порожні запити та фрагменти. |

### Приклади

**Приклад #1 Приклад використання **parse_url()****

` <?php$url = 'http://username:password@hostname:9090/path?arg=value#anchor';var_dump(parse_url($url));var_dump(parse_url($url, PHP_URL_SCHEME));var_dump (parse_url($url,_PHP_URL_USER));var_dump(parse_url($url, PHP_URL_PASS));var_dump(parse_url($url, PHP_URL_HOST));var_dump(parse_url($url,_P PHP_URL_PATH));var_dump(parse_url($url, PHP_URL_QUERY));var_dump(parse_url($url, PHP_URL_FRAGMENT));?> `

Результат виконання цього прикладу:

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

**Приклад #2 Приклад використання **parse_url()** за відсутності
протоколу**

` <?php$url = '//www.example.com/path?googleguy=googley';// До 5.4.7 в path виводилося "//www.example.com/path"var_dump(parse_url($url) );?> `

Результат виконання цього прикладу:

array(3) {
["host"]=>
string(15) "www.example.com"
["path"]=>
string(5) "/path"
["query"]=>
string(17) "googleguy=googley"
}

### Примітки

**Застереження**

Функція може видати некоректні результати для відносних або
недійсні URL-адреси та результати можуть навіть не відповідати
загальної поведінки HTTP-клієнтів. Якщо потрібно проаналізувати
URL-адреси з ненадійних вхідних даних, потрібна додаткова
перевірка, наприклад, за допомогою [filter_var()](function.filter-var.md) з
фільтром **`FILTER_VALIDATE_URL`**.

> **Примітка**:
>
> Ця функція призначена спеціально для аналізу URL-адрес, а не
> URI. Проте, щоб відповідати вимогам зворотної сумісності
> PHP, вона робить виняток для протоколу file://, у якій
> допускаються потрійні сліші (file:///...). Для будь-якого іншого протоколу
> це неприпустимо.

### Дивіться також

- [pathinfo()](function.pathinfo.md) - Повертає інформацію про шлях
до файлу
- [parse_str()](function.parse-str.md) - Розбирає рядок у
змінні
- [http_build_query()](function.http-build-query.md) - Генерує
URL-кодований рядок запиту
- [dirname()](function.dirname.md) - Повертає батьківське ім'я
каталогу із зазначеного шляху
- [basename()](function.basename.md) - Повертає останній
компонент імені із зазначеного шляху
- [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)
