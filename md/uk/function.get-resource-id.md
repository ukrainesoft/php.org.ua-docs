---
navigation:
  - function.get-defined-vars.html: « getdefinedvars
  - function.get-resource-type.html: getresourcetype »
  - index.html: PHP Manual
  - ref.var.html: Функції для роботи зі змінними
title: getresourceід
---
# getresourceід

(PHP 8)

getresourceid — Повертає цілий ідентифікатор для цього ресурсу

### Опис

```methodsynopsis
get_resource_id(resource $resource): int
```

Функція забезпечує безпечний типів спосіб генерації целочисленного ідентифікатора для ресурсу.

### Список параметрів

`resource`

Дескриптор ресурсу

### Значення, що повертаються

Цілочисельний ідентифікатор (int) для зазначеного `resource`

Функція насправді є перетворенням цілого числа (int) від `resource`, щоб спростити отримання ресурсу ідентифікатора.

### Приклади

**Приклад #1 Використання **getresourceid()** дає той самий результат, як і приведення до цілого числа (int)**

```php
<?php

$handle = fopen("php://stdout", "w");

echo (int) $handle . "\n";

echo get_resource_id($handle);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
698
698
```

### Дивіться також

-   [getresourcetype()](function.get-resource-type.html) - Повертає тип ресурсу
