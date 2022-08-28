Повертає всі заголовки HTTP-запиту

-   [« apache\_setenv](function.apache-setenv.html)
    
-   [virtual »](function.virtual.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Apache](ref.apache.html)
    
-   Повертає всі заголовки HTTP-запиту
    

# getallheaders

(PHP 4, PHP 5, PHP 7, PHP 8)

getallheaders — Повертає всі заголовки HTTP-запиту

### Опис

```methodsynopsis
getallheaders(): array
```

Повертає всі заголовки для поточного запиту HTTP.

Ця функція є псевдонімом функції [apache\_request\_headers()](function.apache-request-headers.html). Будь ласка, зверніться до опису функції [apache\_request\_headers()](function.apache-request-headers.html) для отримання детальної інформації про її роботу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив, що містить усі HTTP-заголовки для даного запиту або **`false`** у разі виникнення помилок.

### список змін

| Версия | Описание                               |
|--------|----------------------------------------|
|        | Ця функція стала доступною у SAPI FPM. |

### Приклади

**Приклад #1 Приклад використання **getallheaders()****

```php
<?php

foreach (getallheaders() as $name => $value) {
    echo "$name: $value\n";
}

?>
```

### Дивіться також

-   [apache\_response\_headers()](function.apache-response-headers.html) - Повертає список усіх HTTP-заголовків відповіді Apache