---
navigation:
  - function.curl-multi-errno.html: « curlmultierrno
  - function.curl-multi-getcontent.html: curlmultigetcontent »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlmultiexec
---
# curlmultiexec

(PHP 5, PHP 7, PHP 8)

curlmultiexec — Запускає підключення поточного дескриптора cURL

### Опис

```methodsynopsis
curl_multi_exec(CurlMultiHandle $multi_handle, int &$still_running): int
```

Обробляє кожен дескриптор у стеку. Цей метод може бути викликаний незалежно від необхідності дескриптора читати чи записувати дані.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curlmultiinit()](function.curl-multi-init.html)

`still_running`

Посилання на прапор, який вказує, чи йдуть ще якісь дії.

### Значення, що повертаються

Код cURL, вказаний у [визначених константах](curl.constants.md) CURL.

> **Зауваження**
> 
> Тут повертаються помилки, що стосуються лише всього стеку. Проблеми все ще можуть виникнути на індивідуальних запитах, навіть коли ця функція повертає **`CURLM_OK`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlmultiexec()****

Цей приклад створить два дескриптори cURL, додасть в набір дескрипторів, а потім запустить їх асинхронно.

```php
<?php
// создаём оба ресурса cURL
$ch1 = curl_init();
$ch2 = curl_init();

// устанавливаем URL и другие соответствующие опции
curl_setopt($ch1, CURLOPT_URL, "http://example.com/");
curl_setopt($ch1, CURLOPT_HEADER, 0);
curl_setopt($ch2, CURLOPT_URL, "http://www.php.net/");
curl_setopt($ch2, CURLOPT_HEADER, 0);

//создаём набор дескрипторов cURL
$mh = curl_multi_init();

//добавляем два дескриптора
curl_multi_add_handle($mh,$ch1);
curl_multi_add_handle($mh,$ch2);

//запускаем множественный обработчик
do {
    $status = curl_multi_exec($mh, $active);
    if ($active) {
        // Ждём какое-то время для оживления активности
        curl_multi_select($mh);
    }
} while ($active && $status == CURLM_OK);

//закрываем дескрипторы
curl_multi_remove_handle($mh, $ch1);
curl_multi_remove_handle($mh, $ch2);
curl_multi_close($mh);

?>
```

### Дивіться також

-   [curlmultiinit()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів
-   [curlmultiselect()](function.curl-multi-select.html) - Чекає активності на будь-якому curlmulti з'єднанні
-   [curlexec()](function.curl-exec.html) - Виконує запит cURL
