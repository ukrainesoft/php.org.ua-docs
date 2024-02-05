---
navigation:
  - lua.construct.md: '« Lua::\_\_construct'
  - lua.getversion.md: 'Lua::getVersion »'
  - index.md: PHP Manual
  - class.lua.md: Lua
title: 'Lua::eval'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Lua::eval

(PECL lua >=0.9.0)

Lua::eval — Розбирає рядок як код Lua

### Опис

```methodsynopsis
public Lua::eval(string $statements): mixed
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`statements`

### Значення, що повертаються

Повертає результат виконаного коду, **`null`** у разі некоректних аргументів та \*\*`false`\*\*в случае ошибки.

### Приклади

**Приклад #1 Приклад використання** Lua::eval()\*\*\*\*

```php
<?php
$lua = new Lua();
$lua->eval(<<<CODE
    print(2);
CODE
);
?>
```

Результат виконання наведеного прикладу:

```
2
```
