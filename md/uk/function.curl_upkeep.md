---
navigation:
  - function.curl-unescape.md: « curl\_unescape
  - function.curl-version.md: curl\_version »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_upkeep
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_upkeep

(PHP 8 >= 8.2.0)

curl\_upkeep — Виконує будь-які перевірки працездатності з'єднань

### Опис

```methodsynopsis
curl_upkeep(CurlHandle $handle): bool
```

Доступний при збиранні з libcurl >= 7.62.0.

Деякі протоколи підтримують механізми підтримки з'єднання. Ці механізми зазвичай передають невеликий обсяг трафіку існуючими сполуками, щоб зберегти їх. Це може запобігти закриттю з'єднань, наприклад, через занадто старанних фаєрволів.

В даний час функція підтримки з'єднання доступна лише для з'єднань HTTP/2. Для підтримки з'єднання зазвичай надсилається невеликий обсяг трафіку. HTTP/2 підтримує з'єднання, надсилаючи фрагмент HTTP/2 PING.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**curl\_upkeep()\*\*\*\*

```php
<?php
$url = "https://example.com";

$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, $url);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_HTTP_VERSION,CURL_HTTP_VERSION_2_0);
curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, false);
curl_setopt($ch, CURLOPT_UPKEEP_INTERVAL_MS, 200);
if (curl_exec($ch)) {
    usleep(300);
    var_dump(curl_upkeep($ch));
}
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_init()](function.curl-init.md) \- Ініціалізує сеанс cURL
