---
navigation:
  - generator.current.md: '« Generator::current'
  - generator.key.md: 'Generator::key »'
  - index.md: PHP Manual
  - class.generator.md: Generator
title: 'Generator::getReturn'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Generator::getReturn

(PHP 7, PHP 8)

Generator::getReturn — Отримати значення, що повертається генератором

### Опис

```methodsynopsis
public Generator::getReturn(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Отримує значення генератора, що повертається, після його завершення.

### Приклади

**Пример #1 Пример использования**Generator::getReturn()\*\*\*\*

```php
<?php

$gen = (function() {
    yield 1;
    yield 2;

    return 3;
})();

foreach ($gen as $val) {
    echo $val, PHP_EOL;
}

echo $gen->getReturn(), PHP_EOL;
```

Результат виконання наведеного прикладу:

```
1
2
3
```
