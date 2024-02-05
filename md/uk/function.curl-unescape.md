---
navigation:
  - function.curl-strerror.md: « curl\_strerror
  - function.curl_upkeep.md: curl\_upkeep »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_unescape
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_unescape

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_unescape — Декодує закодований URL-рядок

### Опис

```methodsynopsis
curl_unescape(CurlHandle $handle, string $string): string|false
```

Ця функція декодує закодований URL-рядок.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

`string`

Закодований рядок.

### Значення, що повертаються

Повертає декодований рядок або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования[curl\_escape()](function.curl-escape.md)**

```php
<?php
// Создаём обработчик curl
$ch = curl_init('http://example.com/redirect.php');

// Посылаем HTTP-запрос
curl_setopt($ch, CURLOPT_FOLLOWLOCATION, 1);
curl_exec($ch);

// Получаем последний использованный URL
$effective_url = curl_getinfo($ch, CURLINFO_EFFECTIVE_URL);
// например "http://example.com/show_location.php?loc=M%C3%BCnchen"

// Декодируем
$effective_url_decoded = curl_unescape($ch, $effective_url);
// "http://example.com/show_location.php?loc=München"

// Закрываем обработчик
curl_close($ch);
?>
```

### Примітки

> **Зауваження** :
> 
> Функция**curl\_unescape()** не перетворює плюс (+) у пробіл. Це робить функцію [urldecode()](function.urldecode.md)

### Дивіться також

-   [curl\_escape()](function.curl-escape.md) \- Кодує заданий рядок як URL
-   [urlencode()](function.urlencode.md) \- URL-кодування рядка
-   [urldecode()](function.urldecode.md) \- Декодування URL-кодованого рядка
-   [rawurlencode()](function.rawurlencode.md) \- URL-кодування рядка згідно з RFC 3986
-   [rawurldecode()](function.rawurldecode.md) \- Декодування URL-кодованого рядка
