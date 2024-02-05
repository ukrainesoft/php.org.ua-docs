---
navigation:
  - function.is-real.md: « is\_real
  - function.is-scalar.md: is\_scalar »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_resource
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_resource

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_resource — Перевіряє, чи є змінна ресурс

### Опис

```methodsynopsis
is_resource(mixed $value): bool
```

Перевіряє, чи є змінна ресурс (resource).

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value`— ресурс (resource), иначе\*\*`false`\*\*

### Приклади

**Приклад #1 Приклад використання функції** is\_resource()\*\*\*\*

```php
<?php

$handle = fopen("php://stdout", "w");
if (is_resource($handle)) {
    echo '$handle — это ресурс';
}

?>
```

Результат виконання наведеного прикладу:

```
$handle — это ресурс
```

### Примітки

> **Зауваження** :
> 
> Функция**is\_resource()** перевіряє тип суворо; вона поверне **`false`**, если значение`value` - Це закритий ресурс.

### Дивіться також

-   [Тип resource](language.types.resource.md)
-   [get\_resource\_type()](function.get-resource-type.md) \- Повертає тип ресурсу
