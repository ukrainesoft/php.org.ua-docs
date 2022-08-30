Список опцій контексту CURL

-   [« Опции контекста SSL](context.ssl.md)
    
-   [Контекстні опції Phar »](context.phar.md)
    
-   [PHP Manual](index.md)
    
-   [Контекстні опції та параметри](context.md)
    
-   Список опцій контексту CURL
    

# Опції контексту CURL

Опції контексту CURL - Список опцій контексту CURL

### Опис

Опції контексту CURL доступні, якщо модуль [CURL](intro.curl.md) скомпілюваний, використовуючи конфігураційну опцію **\-with-curlwrappers**

### Опції

`method` string

**`GET`** **`POST`**, або будь-який інший HTTP-метод, що підтримується віддаленим сервером.

За замовчуванням - **`GET`**

`header` string

Додаткові заголовки для надсилання разом із запитом. Значення в цій опції перевизначатимуть інші значення (такі як `User-agent:` `Host:`, і `Authentication:`

`user_agent` string

Значення для надсилання разом із заголовком User-Agent.

За промовчанням використовується значення директиви [useragent](filesystem.configuration.html#ini.user-agent) із файлу php.ini.

`content` string

Додаткові дані для надсилання після заголовків. Ця опція не використовується для запитів **`GET`** або **`HEAD`**

`proxy` string

URI, що вказує адресу проксі-сервера. (Наприклад, `tcp://proxy.example.com:5100`

`max_redirects` int

Максимальна кількість переадресацій, які можна зробити. Значення `1` або менше означає, що жодних переадресацій не буде зроблено.

За замовчуванням `20`

`curl_verify_ssl_host` bool

Перевірити хост.

За замовчуванням **`false`**

> **Зауваження**
> 
> Ця опція доступна для двох обгорток протоколів: http та ftp.

`curl_verify_ssl_peer` bool

Вимагати перевірку використовуваного SSL-сертифіката.

За замовчуванням **`false`**

> **Зауваження**
> 
> Ця опція доступна для двох обгорток протоколів: http та ftp.

### Приклади

**Приклад #1 Отримує сторінку та надсилає POST-запит**

```php
<?php

$postdata = http_build_query(
    array(
        'var1' => 'некоторое содержимое',
        'var2' => 'doh'
    )
);

$opts = array('http' =>
    array(
        'method'  => 'POST',
        'header'  => 'Content-type: application/x-www-form-urlencoded',
        'content' => $postdata
    )
);

$context = stream_context_create($opts);

$result = file_get_contents('http://example.com/submit.php', false, $context);

?>
```

### Дивіться також

-   [Контекстні опції сокету](context.socket.md)