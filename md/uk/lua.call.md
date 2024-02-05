---
navigation:
  - lua.assign.md: '« Lua::assign'
  - lua.construct.md: 'Lua::\_\_construct »'
  - index.md: PHP Manual
  - class.lua.md: Lua
title: 'Lua::call'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Lua::call

# Lua::\_\_call

(PECL lua >=0.9.0)

Lua::call -- Lua::\_\_call — Викликати функції Lua

### Опис

```methodsynopsis
public Lua::call(callable $lua_func, array $args = ?, int $use_self = 0): mixed
```

```methodsynopsis
public Lua::__call(callable $lua_func, array $args = ?, int $use_self = 0): mixed
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`lua_func`

Ім'я функції lua

`args`

Передані аргументи

`use_self`

Чи використовувати `self`

### Значення, що повертаються

Повертає результат функції, що виконалася, **`null`** у разі некоректних аргументів, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**Lua::call()\*\*\*\*

```php
<?php
$lua = new Lua();
$lua->eval(<<<CODE
    function dummy(foo, bar)
        print(foo, ",", bar)
    end
CODE
);
$lua->call("dummy", array("Lua", "geiliable\n"));
$lua->dummy("Lua", "geiliable"); // __call()
var_dump($lua->call(array("table", "concat"), array(array(1=>1, 2=>2, 3=>3), "-")));
?>
```

Результат виконання наведеного прикладу:

```
Lua,geiliable
Lua,geiliable
string(5) "1-2-3"
```

### Дивіться також

-   [\_\_call()](language.oop5.overloading.md#object.call)
