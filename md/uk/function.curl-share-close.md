---
navigation:
  - function.curl-setopt.md: « curlsetopt
  - function.curl-share-errno.md: curlshareerrno »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlshareclose
---
# curlshareclose

(PHP 5> = 5.5.0, PHP 7, PHP 8)

curlshareclose — Закрити роздільний обробник cURL

### Опис

```methodsynopsis
curl_share_close(CurlShareHandle $share_handle): void
```

> **Зауваження**
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Закриває оброблюваний cURL і вивільняє всі його ресурси.

### Список параметрів

`share_handle`

Обробник cURL, що розділяється, повертається [curlshareinit()](function.curl-share-init.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `share_handle` expects a [CurlShareHandle](class.curlsharehandle.md) instance now; Попередньо, як ресурс був виявлений. |

### Приклади

**Приклад #1 Приклад використання [curlsharesetopt()](function.curl-share-setopt.md)**

У цьому прикладі ми створюємо роздільний обробник cURL, додаємо в нього два звичайні обробники і запускаємо їх. Вони будуть використовувати одні й ті ж куки.

```php
<?php
// Создаём разделяемый обработчик и настраиваем его на обмен куками
$sh = curl_share_init();
curl_share_setopt($sh, CURLSHOPT_SHARE, CURL_LOCK_DATA_COOKIE);

// Инициализируем первый обработчик cURL и связываем его с разделяемым
$ch1 = curl_init("http://example.com/");
curl_setopt($ch1, CURLOPT_SHARE, $sh);

// Запускаем первый запрос
curl_exec($ch1);

// Инициализируем второй обработчик cURL и связываем его с разделяемым
$ch2 = curl_init("http://php.net/");
curl_setopt($ch2, CURLOPT_SHARE, $sh);

// Запускаем второй обработчик.
// Ему будут доступны все куки от первого обработчика $ch1
curl_exec($ch2);

// Закрываем разделяемый обработчик
curl_share_close($sh);

// Закрываем оба обычных обработчика
curl_close($ch1);
curl_close($ch2);
?>
```

### Дивіться також

-   [curlshareinit()](function.curl-share-init.md) - Ініціалізація оброблюваного обробника cURL
