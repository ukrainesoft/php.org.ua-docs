---
navigation:
  - function.curl-share-errno.md: « curl\_share\_errno
  - function.curl-share-setopt.md: curl\_share\_setopt »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_share\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_share\_init

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_share\_init — Ініціалізація оброблюваного обробника cURL

### Опис

```methodsynopsis
curl_share_init(): CurlShareHandle
```

Дозволяє різним обробникам cURL ділитися даними один з одним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає оброблюваний cURL.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція повертає екземпляр [CurlShareHandle](class.curlsharehandle.md); раніше, повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання** curl\_share\_init()\*\*\*\*

У цьому прикладі ми створюємо роздільний обробник cURL, додаємо в нього два звичайні обробники і запускаємо їх. Вони будуть використовувати одні й ті ж куки.

```php
<?php
// Создаём разделяемый обработчик и настраиваем его на обмен куками
$sh = curl_share_init();
curl_share_setopt($sh, CURLSHOPT_SHARE, CURL_LOCK_DATA_COOKIE);

// Инициализируем первый обработчик cURL и связываем его с разделяемым
$ch1 = curl_init("http://example.com/");
curl_setopt($ch1, CURLOPT_SHARE, $sh);

// Запускаем первый запрос
curl_exec($ch1);

// Инициализируем второй обработчик cURL и связываем его с разделяемым
$ch2 = curl_init("http://php.net/");
curl_setopt($ch2, CURLOPT_SHARE, $sh);

// Запускаем второй обработчик.
//  Ему будут доступны все куки от первого обработчика $ch1
curl_exec($ch2);

// Закрываем разделяемый обработчик
curl_share_close($sh);

// Закрываем оба обычных обработчика
curl_close($ch1);
curl_close($ch2);
?>
```

### Дивіться також

-   [curl\_share\_setopt()](function.curl-share-setopt.md) \- Встановити опції роздільного оброблювача cURL
-   [curl\_share\_close()](function.curl-share-close.md) \- Закрити оброблюваний обробник cURL
