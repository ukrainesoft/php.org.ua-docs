Ініціалізує сеанс cURL

-   [« curlgetinfo](function.curl-getinfo.html)
    
-   [curlmultiaddhandle »](function.curl-multi-add-handle.html)
    
-   [PHP Manual](index.md)
    
-   [Функции cURL](ref.curl.md)
    
-   Ініціалізує сеанс cURL
    

# curlinit

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

curlinit - Ініціалізує сеанс cURL

### Опис

```methodsynopsis
curl_init(?string $url = null): CurlHandle|false
```

Ініціалізує новий сеанс cURL та повертає дескриптор, який використовується з функціями [curlsetopt()](function.curl-setopt.html) [curlexec()](function.curl-exec.html) і [curlclose()](function.curl-close.html)

### Список параметрів

`url`

Якщо вказано, опція **`CURLOPT_URL`** буде автоматично встановлено значення цього аргументу. Ви можете вручну встановити цю опцію за допомогою функції [curlsetopt()](function.curl-setopt.html)

> **Зауваження**
> 
> Протокол `file` стає недоступним у cURL, якщо задана опція [openbasedir](ini.core.html#ini.open-basedir)

### Значення, що повертаються

Повертає дескриптор cURL у разі успішного виконання та **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У разі успішного виконання повертає екземпляр [CurlHandle](class.curlhandle.md); раніше, повертався ресурс (resource). |
|        | `url` тепер допускає значення null.                                                                                    |

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

-   [curlclose()](function.curl-close.html) - Завершує сеанс cURL
-   [curlmultiinit()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів