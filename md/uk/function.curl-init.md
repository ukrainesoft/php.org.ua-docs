Ініціалізує сеанс cURL

-   [« curl\_getinfo](function.curl-getinfo.html)
    
-   [curl\_multi\_add\_handle »](function.curl-multi-add-handle.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Ініціалізує сеанс cURL
    

# curlinit

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

curlinit - Ініціалізує сеанс cURL

### Опис

```methodsynopsis
curl_init(?string $url = null): CurlHandle|false
```

Ініціалізує новий сеанс cURL та повертає дескриптор, який використовується з функціями [curl\_setopt()](function.curl-setopt.html) [curl\_exec()](function.curl-exec.html) і [curl\_close()](function.curl-close.html)

### Список параметрів

`url`

Якщо вказано, опція **`CURLOPT_URL`** буде автоматично встановлено значення цього аргументу. Ви можете вручну встановити цю опцію за допомогою функції [curl\_setopt()](function.curl-setopt.html)

> **Зауваження**
> 
> Протокол `file` стає недоступним у cURL, якщо задана опція [open\_basedir](ini.core.html#ini.open-basedir)

### Значення, що повертаються

Повертає дескриптор cURL у разі успішного виконання та **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання повертає екземпляр [CurlHandle](class.curlhandle.html); раніше, повертався ресурс (resource). |
|  | `url` тепер допускає значення null. |

### Приклади

**Приклад #1 Ініціалізація нового сеансу cURL та завантаження веб-сторінки**

```php
<?php
// создание нового ресурса cURL
$ch = curl_init();

// установка URL и других необходимых параметров
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// загрузка страницы и выдача её браузеру
curl_exec($ch);

// завершение сеанса и освобождение ресурсов
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_close()](function.curl-close.html) - Завершує сеанс cURL
-   [curl\_multi\_init()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів