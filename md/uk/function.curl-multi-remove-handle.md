Видаляє cURL дескриптор з набору cURL дескрипторів

-   [« curlmultiinit](function.curl-multi-init.html)
    
-   [curlmultiselect »](function.curl-multi-select.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Видаляє cURL дескриптор з набору cURL дескрипторів
    

# curlmultiremovehandle

(PHP 5, PHP 7, PHP 8)

curlmultiremovehandle — Видаляє cURL дескриптор із набору cURL дескрипторів.

### Опис

```methodsynopsis
curl_multi_remove_handle(CurlMultiHandle $multi_handle, CurlHandle $handle): int
```

Видаляє вказаний дескриптор `handle` із зазначеного набору дескрипторів `multi_handle`. Після того, як дескриптор `handle` видалено, його можна знову цілком легально використовувати у функції [curlexec()](function.curl-exec.html). Вилучення дескриптора `handle` під час використання також зупинить поточну передачу на цьому дескрипторі.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curlmultiinit()](function.curl-multi-init.html)

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

### Значення, що повертаються

У разі успішного виконання повертає 0 або одну з констант \*\*`CURLM_XXX`\*\*де XXX - код помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curlinit()](function.curl-init.html) - Ініціалізує сеанс cURL
-   [curlmultiinit()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів
-   [curlmultiaddhandle()](function.curl-multi-add-handle.html) - Додає звичайний cURL-дескриптор до набору cURL-дескрипторів