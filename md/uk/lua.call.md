Викликати функції Lua

-   [« Lua::assign](lua.assign.html)
    
-   [Lua::\_\_construct »](lua.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Lua](class.lua.html)
    
-   Викликати функції Lua
    

# Lua::call

# Lua::call

(PECL lua> = 0.9.0)

Lua::call -- Lua::call — Викликати функції Lua

### Опис

```methodsynopsis
public Lua::call(callable $lua_func, array $args = ?, int $use_self = 0): mixed
```

```methodsynopsis
public Lua::__call(callable $lua_func, array $args = ?, int $use_self = 0): mixed
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`lua_func`

Ім'я функції lua

`args`

Передані аргументи

`use_self`

Чи використовувати `self`

### Значення, що повертаються

Повертає результат функції, що виконалася, **`null`** у разі некоректних аргументів, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Lua::call()****

```php
<?php
$lua = new Lua();
$lua->eval(<<<CODE
    function dummy(foo, bar)
        print(foo, ",", bar)
    end
CODE
);
$lua->call("dummy", array("Lua", "geiliable\n"));
$lua->dummy("Lua", "geiliable"); // __call()
var_dump($lua->call(array("table", "concat"), array(array(1=>1, 2=>2, 3=>3), "-")));
?>
```

Результат виконання цього прикладу:

```
Lua,geiliable
Lua,geiliable
string(5) "1-2-3"
```

### Дивіться також

-   [\_\_call()](language.oop5.overloading.html#object.call)