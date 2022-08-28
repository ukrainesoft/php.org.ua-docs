Повертає список усіх HTTP-заголовків відповіді Apache

-   [« apache\_request\_headers](function.apache-request-headers.html)
    
-   [apache\_setenv »](function.apache-setenv.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Apache](ref.apache.html)
    
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

-   [apache\_request\_headers()](function.apache-request-headers.html) - Отримує список усіх заголовків HTTP-запиту
-   [headers\_sent()](function.headers-sent.html) - Перевіряє, чи були надіслані заголовки
-   [headers\_list()](function.headers-list.html) - Повертає список переданих заголовків (або готових до відправлення)