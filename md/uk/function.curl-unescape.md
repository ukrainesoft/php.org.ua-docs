---
navigation:
  - function.curl-strerror.html: « curlstrerror
  - function.curl-version.html: curlversion »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlunescape
---
# curlunescape

(PHP 5> = 5.5.0, PHP 7, PHP 8)

curlunescape — Декодує закодований URL-рядок

### Опис

```methodsynopsis
curl_unescape(CurlHandle $handle, string $string): string|false
```

Ця функція декодує закодований URL-рядок.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

`string`

Закодований рядок.

### Значення, що повертаються

Повертає декодований рядок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання [curlescape()](function.curl-escape.html)**

```php
<?php
// Создаём обработчик curl
$ch = curl_init('http://example.com/redirect.php');

// Посылаем HTTP-запрос
curl_setopt($ch, CURLOPT_FOLLOWLOCATION, 1);
curl_exec($ch);

// Получаем последний использованный URL
$effective_url = curl_getinfo($ch, CURLINFO_EFFECTIVE_URL);
// например "http://example.com/show_location.php?loc=M%C3%BCnchen"

// Декодируем
$effective_url_decoded = curl_unescape($ch, $effective_url);
// "http://example.com/show_location.php?loc=München"

// Закрываем обработчик
curl_close($ch);
?>
```

### Примітки

> **Зауваження**
> 
> **curlunescape()** не перетворює плюс (+) у пробіл. Це робить функцію [urldecode()](function.urldecode.md)

### Дивіться також

-   [curlescape()](function.curl-escape.html) - Кодує заданий рядок як URL
-   [urlencode()](function.urlencode.md) - URL-кодування рядка
-   [urldecode()](function.urldecode.md) - Декодування URL-кодованого рядка
-   [rawurlencode()](function.rawurlencode.md) - URL-кодування рядка згідно з RFC 3986
-   [rawurldecode()](function.rawurldecode.md) - Декодування URL-кодованого рядка
