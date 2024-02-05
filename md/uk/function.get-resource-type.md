---
navigation:
  - function.get-resource-id.md: « get\_resource\_id
  - function.gettype.md: gettype »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: get\_resource\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_resource\_type

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

get\_resource\_type — Повертає тип ресурсу

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

Функція повертає **`null`** і викликає помилку, якщо `resource` перестав бути ресурсом (resource).

### Приклади

**Пример #1 Пример использования**get\_resource\_type()\*\*\*\*

```php
<?php

// Начиная с версии PHP 8.0.0, следующий код больше не работает. Функция curl_init теперь возвращает объект CurlHandle.
$c = curl_init();
echo get_resource_type($c) . "\n";
?>
```

Результат виконання наведеного прикладу в PHP 7:

```
stream
curl
```

### Дивіться також

-   [get\_resource\_id()](function.get-resource-id.md) \- Повертає цілий ідентифікатор для даного ресурсу
