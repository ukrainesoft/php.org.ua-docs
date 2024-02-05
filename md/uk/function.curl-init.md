---
navigation:
  - function.curl-getinfo.md: « curl\_getinfo
  - function.curl-multi-add-handle.md: curl\_multi\_add\_handle »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_init

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

curl\_init - Ініціалізує сеанс cURL

### Опис

```methodsynopsis
curl_init(?string $url = null): CurlHandle|false
```

Ініціалізує новий сеанс cURL та повертає дескриптор, який використовується з функціями [curl\_setopt()](function.curl-setopt.md) [curl\_exec()](function.curl-exec.md) і [curl\_close()](function.curl-close.md)

### Список параметрів

`url`

Якщо вказано, опція **`CURLOPT_URL`** буде автоматично встановлено значення цього аргументу. Ви можете вручну встановити цю опцію за допомогою функції [curl\_setopt()](function.curl-setopt.md)

> **Зауваження** :
> 
> Протокол`file` стає недоступним у cURL, якщо задана опція [open\_basedir](ini.core.md#ini.open-basedir)

### Значення, що повертаються

Повертає дескриптор cURL у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання повертає екземпляр [CurlHandle](class.curlhandle.md); раніше, повертався ресурс (resource). |
| 8.0.0 | `url` тепер допускає значення null. |

### Приклади

**Приклад #1 Ініціалізація нового сеансу cURL та завантаження веб-сторінки**

```php
<?php
// создание нового ресурса cURL
$ch = curl_init();

// установка URL и других необходимых параметров
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// загрузка страницы и выдача её браузеру
curl_exec($ch);

// завершение сеанса и освобождение ресурсов
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_close()](function.curl-close.md) \- Завершує сеанс cURL
-   [curl\_multi\_init()](function.curl-multi-init.md) \- Створює набір cURL-дескрипторів
