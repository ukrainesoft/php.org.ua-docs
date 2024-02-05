---
navigation:
  - class.luaclosure.md: « LuaClosure
  - book.luasandbox.md: LuaSandbox »
  - index.md: PHP Manual
  - class.luaclosure.md: LuaClosure
title: 'LuaClosure::\_\_invoke'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaClosure::\_\_invoke

(PECL lua >=0.9.0)

LuaClosure::\_\_invoke — Виклик замикання Lua

### Опис

```methodsynopsis
public LuaClosure::__invoke(mixed ...$args): void
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`args`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання**LuaClosure::\_\_invoke()\*\*\*\*

```php
<?php
$lua = new Lua();
$closure = $lua->eval(<<<CODE
    return (function ()
        print("hello world")
    end)
CODE
);

$lua->call($closure);
$closure();
?>
```

Результат виконання наведеного прикладу:

```
hello worldhello world
```
