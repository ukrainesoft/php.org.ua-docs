---
navigation:
  - function.apache-setenv.html: « apachesetenv
  - function.virtual.md: virtual »
  - index.md: PHP Manual
  - ref.apache.md: Функции Apache
title: getallheaders
---
# getallheaders

(PHP 4, PHP 5, PHP 7, PHP 8)

getallheaders — Повертає всі заголовки HTTP-запиту

### Опис

```methodsynopsis
getallheaders(): array
```

Повертає всі заголовки для поточного запиту HTTP.

Ця функція є псевдонімом функції [apacherequestheaders()](function.apache-request-headers.html). Будь ласка, зверніться до опису функції [apacherequestheaders()](function.apache-request-headers.md) для отримання детальної інформації про її роботу.

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

-   [apacheresponseheaders()](function.apache-response-headers.md) - Повертає список усіх HTTP-заголовків відповіді Apache
