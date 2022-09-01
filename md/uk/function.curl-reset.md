---
navigation:
  - function.curl-pause.html: « curlpause
  - function.curl-setopt-array.html: curlsetoptarray »
  - index.html: PHP Manual
  - ref.curl.html: Функции cURL
title: curlreset
---
# curlreset

(PHP 5> = 5.5.0, PHP 7, PHP 8)

curlreset — Скинути всі налаштування обробника сесії libcurl

### Опис

```methodsynopsis
curl_reset(CurlHandle $handle): void
```

Ця функція переініціалізує всі параметри заданого оброблювача сесії cURL за промовчанням.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlreset()****

```php
<?php
// Создаём обработчик curl
$ch = curl_init();

// Устанавливаем опцию CURLOPT_USERAGENT
curl_setopt($ch, CURLOPT_USERAGENT, "My test user-agent");

// Сбрасываем все установленные опции
curl_reset($ch);

// Посылаем запрос HTTP
curl_setopt($ch, CURLOPT_URL, 'http://example.com/');
curl_exec($ch); // установленный ранее user-agent сброшен

// Закрываем обработчик
curl_close($ch);
?>
```

### Примітки

> **Зауваження**
> 
> **curlreset()** також скидає URL, заданий як параметр [curlinit()](function.curl-init.html)

### Дивіться також

-   [curlsetopt()](function.curl-setopt.html) - Встановлює параметр для сеансу CURL
