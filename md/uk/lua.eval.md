---
navigation:
  - lua.construct.md: '« Lua::construct'
  - lua.getversion.md: 'Lua::getVersion »'
  - index.md: PHP Manual
  - class.lua.md: Lua
title: 'Lua::eval'
---
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
$lua = new Lua();
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
