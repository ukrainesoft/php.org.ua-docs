---
navigation:
  - function.curl-close.md: « curl\_close
  - function.curl-errno.md: curl\_errno »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_copy\_handle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_copy\_handle

(PHP 5, PHP 7, PHP 8)

curl\_copy\_handle — Копіює дескриптор cURL разом із усіма його налаштуваннями

### Опис

```methodsynopsis
curl_copy_handle(CurlHandle $handle): CurlHandle|false
```

Копіює дескриптор cURL, зберігаючи його налаштування.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Повертає новий дескриптор cURL або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |
| 8.0.0 | У разі успішного виконання повертає екземпляр [CurlHandle](class.curlhandle.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Копіювання дескриптора cURL**

```php
<?php
// создание нового ресурса cURL
$ch = curl_init();

// установка URL и других соответствующих параметров
curl_setopt($ch, CURLOPT_URL, 'http://www.example.com/');
curl_setopt($ch, CURLOPT_HEADER, 0);

// копирование дескриптора
$ch2 = curl_copy_handle($ch);

// загрузка URL (http://www.example.com/) и её передача в браузер
curl_exec($ch2);

// закрытие ресурсов cURL и освобождение системных ресурсов
curl_close($ch2);
curl_close($ch);
?>
```
