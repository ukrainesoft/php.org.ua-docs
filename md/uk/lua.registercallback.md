Зареєструвати функцію PHP у Lua

-   [« Lua::include](lua.include.html)
    
-   [LuaClosure »](class.luaclosure.html)
    
-   [PHP Manual](index.html)
    
-   [Lua](class.lua.html)
    
-   Зареєструвати функцію PHP у Lua
    

# Lua::registerCallback

(No version information available, might only be in Git)

Lua::registerCallback — Зареєструвати функцію PHP у Lua

### Опис

```methodsynopsis
public Lua::registerCallback(string $name, callable $function): mixed
```

Реєструє функцію PHP у Lua з ім'ям "$name"

### Список параметрів

`name`

`function`

Коректна функція зворотного виклику PHP

### Значення, що повертаються

Повертає $this, **`null`** у разі некоректних аргументів, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Lua::registerCallback()****

```php
<?php
$lua = new Lua();
$lua->registerCallback("echo", "var_dump");
$lua->eval(<<<CODE
    echo({1, 2, 3});
CODE
);
?>
```

Результат виконання цього прикладу:

```
array(3) {
  [1]=>
  float(1)
  [2]=>
  float(2)
  [3]=>
  float(3)
}
```