Розбирає рядок як код Lua

-   [« Lua::construct](lua.construct.html)
    
-   [Lua::getVersion »](lua.getversion.html)
    
-   [PHP Manual](index.html)
    
-   [Lua](class.lua.html)
    
-   Розбирає рядок як код Lua
    

# Lua::eval

(PECL lua> = 0.9.0)

Lua::eval — Розбирає рядок як код Lua

### Опис

```methodsynopsis
public Lua::eval(string $statements): mixed
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`statements`

### Значення, що повертаються

Повертає результат виконаного коду, **`null`** у разі некоректних аргументів та **`false`** у разі помилки.

### Приклади

**Приклад #1 Приклад використання **Lua::eval()****

```php
<?php
$lua = new Lua();
$lua->eval(<<<CODE
    print(2);
CODE
);
?>
```

Результат виконання цього прикладу:

```
2
```