---
navigation:
  - function.uopz-get-property.md: « uopz\_get\_property
  - function.uopz-get-static.md: uopz\_get\_static »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_get\_return
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_get\_return

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_get\_return — Отримує попереднє встановлене значення, що повертається для функції

### Опис

```methodsynopsis
uopz_get_return(string $function): mixed
```

```methodsynopsis
uopz_get_return(string $class, string $function): mixed
```

Получает возвращаемое значение`function`, ранее установленное с помощью[uopz\_set\_return()](function.uopz-set-return.md)

### Список параметрів

`class`

Ім'я класу, що містить функцію

`function`

Ім'я функції

### Значення, що повертаються

Раніше встановлено значення або об'єкт Closure.

### Приклади

**Приклад #1 Приклад використання** uopz\_get\_return()\*\*\*\*

```php
<?php
uopz_set_return("strlen", 42);
echo uopz_get_return("strlen");
?>
```

Результат виконання наведеного прикладу:

```
42
```
