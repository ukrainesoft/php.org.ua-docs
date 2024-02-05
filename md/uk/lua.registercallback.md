---
navigation:
  - lua.include.md: '« Lua::include'
  - class.luaclosure.md: LuaClosure »
  - index.md: PHP Manual
  - class.lua.md: Lua
title: 'Lua::registerCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Возвращает $this,**`null`** у разі некоректних аргументів, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Lua::registerCallback()\*\*\*\*

```php
<?php
$lua = new Lua();
$lua->registerCallback("echo", "var_dump");
$lua->eval(<<<CODE
    echo({1, 2, 3});
CODE
);
?>
```

Результат виконання наведеного прикладу:

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
