---
navigation:
  - function.curl-pause.md: « curl\_pause
  - function.curl-setopt-array.md: curl\_setopt\_array »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_reset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_reset

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_reset — Скинути всі налаштування обробника сесії libcurl

### Опис

```methodsynopsis
curl_reset(CurlHandle $handle): void
```

Ця функція переініціалізує всі параметри заданого оброблювача сесії cURL за промовчанням.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_reset()\*\*\*\*

```php
<?php
// Создаём обработчик curl
$ch = curl_init();

// Устанавливаем опцию CURLOPT_USERAGENT
curl_setopt($ch, CURLOPT_USERAGENT, "My test user-agent");

// Сбрасываем все установленные опции
curl_reset($ch);

// Посылаем запрос HTTP
curl_setopt($ch, CURLOPT_URL, 'http://example.com/');
curl_exec($ch); // установленный ранее user-agent сброшен

// Закрываем обработчик
curl_close($ch);
?>
```

### Примітки

> **Зауваження** :
> 
> **curl\_reset()** також скидає URL, заданий як параметр [curl\_init()](function.curl-init.md)

### Дивіться також

-   [curl\_setopt()](function.curl-setopt.md) \- Встановлює параметр для передачі cURL
