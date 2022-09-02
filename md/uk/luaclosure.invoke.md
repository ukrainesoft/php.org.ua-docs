---
navigation:
  - class.luaclosure.md: « LuaClosure
  - book.luasandbox.md: LuaSandbox »
  - index.md: PHP Manual
  - class.luaclosure.md: LuaClosure
title: 'LuaClosure::invoke'
---
# LuaClosure::invoke

(PECL lua> = 0.9.0)

LuaClosure::invoke — Виклик замикання Lua

### Опис

```methodsynopsis
public LuaClosure::__invoke(mixed ...$args): void
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`args`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання**LuaClosure::invoke()\*\*\*\*

```php
<?php
$lua = new Lua();
$closure = $lua->eval(<<<CODE
    return (function ()
        print("hello world")
    end)
CODE
);

$lua->call($closure);
$closure();
?>
```

Результат виконання цього прикладу:

```
hello worldhello world
```
