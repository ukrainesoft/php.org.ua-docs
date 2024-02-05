---
navigation:
  - function.get-defined-vars.md: « get\_defined\_vars
  - function.get-resource-type.md: get\_resource\_type »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: get\_resource\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_resource\_id

(PHP 8)

get\_resource\_id — Повертає цілий ідентифікатор для цього ресурсу

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

**Приклад #1 Использование**get\_resource\_id()\*\* дає той самий результат, як і приведення до цілого числа (int)\*\*

```php
<?php

$handle = fopen("php://stdout", "w");

echo (int) $handle . "\n";

echo get_resource_id($handle);

?>
```

Висновок наведеного прикладу буде схожим на:

```
698
698
```

### Дивіться також

-   [get\_resource\_type()](function.get-resource-type.md) \- Повертає тип ресурсу
