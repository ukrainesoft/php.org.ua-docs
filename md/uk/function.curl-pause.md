Зупинити та відновити з'єднання

-   [« curlmultistrerror](function.curl-multi-strerror.html)
    
-   [curlreset »](function.curl-reset.html)
    
-   [PHP Manual](index.md)
    
-   [Функции cURL](ref.curl.md)
    
-   Зупинити та відновити з'єднання
    

# curlpause

(PHP 5> = 5.5.0, PHP 7, PHP 8)

curlpause — Зупинити та відновити з'єднання

### Опис

```methodsynopsis
curl_pause(CurlHandle $handle, int $flags): int
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

`flags`

Одна з констант **`CURLPAUSE_*`**

### Значення, що повертаються

Повертає один із кодів повернення (**`CURLE_OK`** якщо помилок немає).

### список змін

| Версия | Описание                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------|
|        | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |