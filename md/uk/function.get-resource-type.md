Повертає тип ресурсу

-   [« getresourceід](function.get-resource-id.html)
    
-   [gettype »](function.gettype.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи зі змінними](ref.var.html)
    
-   Повертає тип ресурсу
    

# getresourcetype

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

getresourcetype — Повертає тип ресурсу

### Опис

```methodsynopsis
get_resource_type(resource $resource): string
```

Функція повертає тип ресурсу.

### Список параметрів

`resource`

Визначається дескриптор ресурсу.

### Значення, що повертаються

Якщо цей параметр `resource` є ресурсом, функція повертає рядок, що вказує на його тип. Якщо тип не визначається цією функцією, значенням, що повертається, буде рядок `Unknown`

Функція повертає **`null`** і викликає помилку, якщо `resource` не є ресурсом (resource).

### Приклади

**Приклад #1 Приклад використання **getresourcetype()****

```php
<?php

// Начиная с версии PHP 8.0.0, следующий код больше не работает. Функция curl_init теперь возвращает объект CurlHandle.
$c = curl_init();
echo get_resource_type($c) . "\n";
?>
```

Результат виконання цього прикладу в PHP 7:

```
stream
curl
```

### Дивіться також

-   [getresourceid()](function.get-resource-id.html) - Повертає цілий ідентифікатор для даного ресурсу