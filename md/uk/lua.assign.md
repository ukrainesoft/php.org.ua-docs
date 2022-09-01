---
navigation:
  - class.lua.html: « Lua
  - lua.call.html: 'Lua::call »'
  - index.html: PHP Manual
  - class.lua.html: Lua
title: 'Lua::assign'
---
# Lua::assign

(PECL lua> = 0.9.0)

Lua::assign — Присвоїти PHP-змінній Lua

### Опис

```methodsynopsis
public Lua::assign(string $name, string $value): mixed
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`name`

`value`

### Значення, що повертаються

Повертає $this або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Lua::assign()****

```php
<?php
$lua = new Lua();
$lua->assign("php_var", array(1=>1, 2, 3)); // индексы таблицы lua начинаются с 1
$lua->eval(<<<CODE
    print(php_var);
CODE
);
?>
```

Результат виконання цього прикладу:

```
Array
 (
     [1] => 1
     [2] => 2
     [3] => 3
 )
```
