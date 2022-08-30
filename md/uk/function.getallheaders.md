Повертає всі заголовки HTTP-запиту

-   [« apachesetenv](function.apache-setenv.html)
    
-   [virtual »](function.virtual.md)
    
-   [PHP Manual](index.md)
    
-   [Функции Apache](ref.apache.md)
    
-   Повертає всі заголовки HTTP-запиту
    

# getallheaders

(PHP 4, PHP 5, PHP 7, PHP 8)

getallheaders — Повертає всі заголовки HTTP-запиту

### Опис

```methodsynopsis
getallheaders(): array
```

Повертає всі заголовки для поточного запиту HTTP.

Ця функція є псевдонімом функції [apacherequestheaders()](function.apache-request-headers.html). Будь ласка, зверніться до опису функції [apacherequestheaders()](function.apache-request-headers.html) для отримання детальної інформації про її роботу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив, що містить усі HTTP-заголовки для даного запиту або **`false`** у разі виникнення помилок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Ця функція стала доступною у SAPI FPM. |

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

-   [apacheresponseheaders()](function.apache-response-headers.html) - Повертає список усіх HTTP-заголовків відповіді Apache