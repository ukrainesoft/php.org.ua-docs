---
navigation:
  - function.uopz-compose.md: « uopz\_compose
  - function.uopz-del-function.md: uopz\_del\_function »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_copy

(PECL uopz 1 >= 1.0.4, PECL uopz 2)

uopz\_copy — Копіювати функцію

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_copy(string $function): Closure
```

```methodsynopsis
uopz_copy(string $class, string $function): Closure
```

Копіювати функцію на ім'я

### Список параметрів

`class`

Ім'я класу, що містить функцію копіювання

`function`

Ім'я функції

### Значення, що повертаються

Об'єкт Closure для певної функції

### Приклади

**Пример #1 Пример использования**uopz\_copy()\*\*\*\*

```php
<?php
$strtotime = uopz_copy('strtotime');

uopz_function("strtotime", function($arg1, $arg2) use($strtotime) {
    /* зесь можно вызвать оригинальную функцию strtotime */
    var_dump($arg1);
});

var_dump(strtotime('dummy'));
?>
```

Результат виконання наведеного прикладу:

```
string(5) "dummy"
```
