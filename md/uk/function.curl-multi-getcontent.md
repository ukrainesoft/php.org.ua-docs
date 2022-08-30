Повертає результат операції, якщо було встановлено опцію CURLOPTRETURNTRANSFER

-   [« curlmultiexec](function.curl-multi-exec.html)
    
-   [curlmultiinforead »](function.curl-multi-info-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Повертає результат операції, якщо було встановлено опцію CURLOPTRETURNTRANSFER
    

# curlmultigetcontent

(PHP 5, PHP 7, PHP 8)

curlmultigetcontent — Повернення результату операції, якщо встановлено опцію **`CURLOPT_RETURNTRANSFER`**

### Опис

```methodsynopsis
curl_multi_getcontent(CurlHandle $handle): ?string
```

Якщо для певного дескриптора було встановлено опцію \*\*`CURLOPT_RETURNTRANSFER`\*\*ця функція поверне вміст цього cURL-дескриптора у вигляді рядка.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

### Значення, що повертаються

Повертає вміст cURL-дескриптора, якщо була використана опція **`CURLOPT_RETURNTRANSFER`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curlmultiinit()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів