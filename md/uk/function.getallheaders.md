---
navigation:
  - function.apache-setenv.md: « apache\_setenv
  - function.virtual.md: virtual »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: getallheaders
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getallheaders

(PHP 4, PHP 5, PHP 7, PHP 8)

getallheaders — Повертає всі заголовки HTTP-запиту

### Опис

```methodsynopsis
getallheaders(): array
```

Повертає всі заголовки для поточного запиту HTTP.

Ця функція є псевдонімом функції [apache\_request\_headers()](function.apache-request-headers.md)Пожалуйста, обратитесь к описанию функции[apache\_request\_headers()](function.apache-request-headers.md) для отримання детальної інформації про її роботу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив, що містить усі HTTP-заголовки для даного запиту або \*\*`false`\*\*в случае возникновения ошибок.

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Ця функція стала доступною у SAPI FPM. |

### Приклади

**Приклад #1 Приклад використання** getallheaders()\*\*\*\*

```php
<?php

foreach (getallheaders() as $name => $value) {
    echo "$name: $value\n";
}

?>
```

### Дивіться також

-   [apache\_response\_headers()](function.apache-response-headers.md) \- Повертає список усіх HTTP-заголовків відповіді Apache
