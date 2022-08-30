Повертає список усіх HTTP-заголовків відповіді Apache

-   [« apacherequestheaders](function.apache-request-headers.html)
    
-   [apachesetenv »](function.apache-setenv.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Apache](ref.apache.md)
    
-   Повертає список усіх HTTP-заголовків відповіді Apache
    

# apacheresponseheaders

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

apacheresponseheaders — Повертає список усіх заголовків HTTP відповіді Apache

### Опис

```methodsynopsis
apache_response_headers(): array|false
```

Повертає список усіх заголовків HTTP. Працює на веб-серверах Apache та FastCGI.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив HTTP-заголовків відповіді Apache у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apacheresponseheaders()****

```php
<?php
print_r(apache_response_headers());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [Accept-Ranges] => bytes
    [X-Powered-By] => PHP/4.3.8
)
```

### Дивіться також

-   [apacherequestheaders()](function.apache-request-headers.html) - Отримує список усіх заголовків HTTP-запиту
-   [headerssent()](function.headers-sent.html) - Перевіряє, чи були надіслані заголовки
-   [headerslist()](function.headers-list.html) - Повертає список переданих заголовків (або готових до відправлення)