---
navigation:
  - function.curl-share-init.md: « curl\_share\_init
  - function.curl-share-strerror.md: curl\_share\_strerror »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_share\_setopt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_share\_setopt

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_share\_setopt — Встановити опції роздільного обробника cURL

### Опис

```methodsynopsis
curl_share_setopt(CurlShareHandle $share_handle, int $option, mixed $value): bool
```

Встановлює опції оброблюваного cURL.

### Список параметрів

`share_handle`

Обробник, що розділяється cURL, повертається [curl\_share\_init()](function.curl-share-init.md)

`option`

| Опция | Опис |
| --- | --- |
| **`CURLSHOPT_SHARE`** | Задає тип даних, які потрібно розділяти. |
| **`CURLSHOPT_UNSHARE`** | Вказує тип даних, які більше не треба розділяти. |

`value`

| Значение | Опис |
| --- | --- |
| **`CURL_LOCK_DATA_COOKIE`** | Поділяє дані cookie. |
| **`CURL_LOCK_DATA_DNS`** | Розділяє кеш DNS. Зверніть увагу, що якщо ви використовуєте множинний обробник cURL, всі додані обробники за умовчанням будуть розділяти DNS-кеш. |
| **`CURL_LOCK_DATA_SSL_SESSION`** | Розділяє ідентифікатори сесії SSL, скорочуючи час, що витрачається на підтвердження (handshake) SSL при повторному з'єднанні з тим самим сервером. Зверніть увагу, що ідентифікатори сесії SSL за замовчуванням перевикористовуватимуться тим самим обробником. |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `share_handle` expects a [CurlShareHandle](class.curlsharehandle.md) instance now; previously, a resource was expected. |

### Приклади

**Приклад #1 Приклад використання** curl\_share\_setopt()\*\*\*\*

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
