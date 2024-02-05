---
navigation:
  - function.apache-request-headers.md: « apache\_request\_headers
  - function.apache-setenv.md: apache\_setenv »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_response\_headers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_response\_headers

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

apache\_response\_headers — Повертає список усіх заголовків HTTP відповіді Apache

### Опис

```methodsynopsis
apache_response_headers(): array|false
```

Повертає список усіх заголовків HTTP. Працює на веб-серверах Apache та FastCGI.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив HTTP-заголовків відповіді Apache у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** apache\_response\_headers()\*\*\*\*

```php
<?php
print_r(apache_response_headers());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [Accept-Ranges] => bytes
    [X-Powered-By] => PHP/4.3.8
)
```

### Дивіться також

-   [apache\_request\_headers()](function.apache-request-headers.md) \- Отримує список усіх заголовків HTTP-запиту
-   [headers\_sent()](function.headers-sent.md) \- Перевіряє, чи були надіслані заголовки
-   [headers\_list()](function.headers-list.md) \- Повертає список переданих заголовків (або готових до відправлення)
