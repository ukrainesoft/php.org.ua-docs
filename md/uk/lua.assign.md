---
navigation:
  - class.lua.md: « Lua
  - lua.call.md: 'Lua::call »'
  - index.md: PHP Manual
  - class.lua.md: Lua
title: 'Lua::assign'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Lua::assign

(PECL lua >=0.9.0)

Lua::assign — Присвоїти PHP-змінній Lua

### Опис

```methodsynopsis
public Lua::assign(string $name, string $value): mixed
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`name`

`value`

### Значення, що повертаються

Повертає $this або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Lua::assign()\*\*\*\*

```php
<?php
$lua = new Lua();
$lua->assign("php_var", array(1=>1, 2, 3)); // индексы таблицы lua начинаются с 1
$lua->eval(<<<CODE
    print(php_var);
CODE
);
?>
```

Результат виконання наведеного прикладу:

```
Array
 (
     [1] => 1
     [2] => 2
     [3] => 3
 )
```
