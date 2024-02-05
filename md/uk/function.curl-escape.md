---
navigation:
  - function.curl-error.md: « curl\_error
  - function.curl-exec.md: curl\_exec »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_escape
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_escape

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_escape — Кодує заданий рядок як URL

### Опис

```methodsynopsis
curl_escape(CurlHandle $handle, string $string): string|false
```

Кодирует строку согласно[» RFC 3986](http://www.faqs.org/rfcs/rfc3986)

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

`string`

Рядок для кодування.

### Значення, що повертаються

Повертає екранований рядок або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_escape()\*\*\*\*

```php
<?php
// Создаём обработчик curl
$ch = curl_init();

// Экранируем строку, которую хотим передать методом GET
$location = curl_escape($ch, 'Hofbräuhaus / München');
// Результат: Hofbr%C3%A4uhaus%20%2F%20M%C3%BCnchen

// Собираем URL по частям
$url = "http://example.com/add_location.php?location={$location}";
// Результат: http://example.com/add_location.php?location=Hofbr%C3%A4uhaus%20%2F%20M%C3%BCnchen

// Посылаем запрос HTTP и закрываем обработчик
curl_setopt($ch, CURLOPT_URL, $url);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_exec($ch);
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_unescape()](function.curl-unescape.md) \- Декодує закодований URL-рядок
-   [urlencode()](function.urlencode.md) \- URL-кодування рядка
-   [rawurlencode()](function.rawurlencode.md) \- URL-кодування рядка згідно з RFC 3986
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)
