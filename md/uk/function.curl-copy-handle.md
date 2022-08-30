Копіює дескриптор cURL разом із усіма його налаштуваннями

-   [« curlclose](function.curl-close.html)
    
-   [curlerrno »](function.curl-errno.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Копіює дескриптор cURL разом із усіма його налаштуваннями
    

# curlcopyhandle

(PHP 5, PHP 7, PHP 8)

curlcopyhandle — Копіює дескриптор cURL разом із усіма його налаштуваннями

### Опис

```methodsynopsis
curl_copy_handle(CurlHandle $handle): CurlHandle|false
```

Копіює дескриптор cURL, зберігаючи його налаштування.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

### Значення, що повертаються

Повертає новий дескриптор cURL або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |
|  | У разі успішного виконання повертає екземпляр [CurlHandle](class.curlhandle.html); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Копіювання дескриптора cURL**

```php
<?php
// создание нового ресурса cURL
$ch = curl_init();

// установка URL и других соответствующих параметров
curl_setopt($ch, CURLOPT_URL, 'http://www.example.com/');
curl_setopt($ch, CURLOPT_HEADER, 0);

// копирование дескриптора
$ch2 = curl_copy_handle($ch);

// загрузка URL (http://www.example.com/) и её передача в браузер
curl_exec($ch2);

// закрытие ресурсов cURL и освобождение системных ресурсов
curl_close($ch2);
curl_close($ch);
?>
```