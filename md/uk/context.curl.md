- [« Опції контексту SSL](context.ssl.md)
- [Контекстні опції Phar »](context.phar.md)

- [PHP Manual](index.md)
- [Контекстні опції та параметри](context.md)
- Список опцій контексту CURL

# Опції контексту CURL

Опції контексту CURL - Список опцій контексту CURL

### Опис

Опції контексту CURL доступні, якщо модуль
[CURL](intro.curl.md) скомпілюваний, використовуючи конфігураційну опцію
**--with-curlwrappers**.

### Опції

`method` string
**`GET`**, **`POST`**, або будь-який інший HTTP-метод, що підтримується
віддаленим сервером.

За замовчуванням – **`GET`**.

`header` string
Додаткові заголовки для надсилання разом із запитом. Значення у цій
опції будуть перевизначати інші значення (такі як User-agent:,
`Host:`, та `Authentication:`).

`user_agent` string
Значення для надсилання разом із заголовком User-Agent.

За замовчуванням використовується значення директиви
[user_agent](filesystem.configuration.md#ini.user-agent) з файлу
`php.ini`.

`content` string
Додаткові дані для надсилання після заголовків. Ця опція не
використовується для запитів **`GET`** або **`HEAD`**.

`proxy` string
URI, який вказує адресу проксі-сервера. (Наприклад,
`tcp://proxy.example.com:5100`).

`max_redirects` int
Максимальна кількість переадресацій, які можна зробити. Значення
`1` або менше означає, що жодних переадресацій не буде зроблено.

Типово `20`.

`curl_verify_ssl_host` bool
Перевірити хост.

Типово **`false`**

> **Примітка**:
>
> Ця опція доступна для двох обгорток протоколів: http та ftp.

`curl_verify_ssl_peer` bool
Вимагати перевірку використовуваного SSL-сертифіката.

Типово **`false`**

> **Примітка**:
>
> Ця опція доступна для двох обгорток протоколів: http та ftp.

### Приклади

**Приклад #1 Отримує сторінку та надсилає POST-запит**

` <?php$postdata = http_build_query(    array(        'var1' => 'некоторое содержимое',        'var2' => 'doh'    ));$opts = array('http' =>    array(        'method'  => ' POST',         ¦                                     ¦¦ ://example.com/submit.php', false, $context);?> `

### Дивіться також

- [Контекстні опції сокету](context.socket.md)
