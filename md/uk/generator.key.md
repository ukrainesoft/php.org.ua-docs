---
navigation:
  - generator.getreturn.md: '« Generator::getReturn'
  - generator.next.md: 'Generator::next »'
  - index.md: PHP Manual
  - class.generator.md: Generator
title: 'Generator::key'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Generator::key

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

Generator::key — Отримати ключ згенерованого елемента

### Опис

```methodsynopsis
public Generator::key(): mixed
```

Отримує ключ згенерованого елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ключ згенерованого елемента.

### Приклади

**Приклад #1 Приклад використання** Generator::key()\*\*\*\*

```php
<?php

function Gen()
{
    yield 'key' => 'value';
}

$gen = Gen();

echo "{$gen->key()} => {$gen->current()}";
```

Результат виконання наведеного прикладу:

```
key => value
```
