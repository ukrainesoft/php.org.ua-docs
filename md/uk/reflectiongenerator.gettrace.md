---
navigation:
  - reflectiongenerator.getthis.md: '« ReflectionGenerator::getThis'
  - class.reflectionfiber.md: ReflectionFiber »
  - index.md: PHP Manual
  - class.reflectiongenerator.md: ReflectionGenerator
title: 'ReflectionGenerator::getTrace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionGenerator::getTrace

(PHP 7, PHP 8)

ReflectionGenerator::getTrace — Отримати трасування запущеного генератора

### Опис

```methodsynopsis
public ReflectionGenerator::getTrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT): array
```

Повертає трасування запущеного генератора.

### Список параметрів

`options`

Значение`options` може бути одним з наступних прапорів:

**Доступні опції**

| Опция | Опис |
| --- | --- |
| **`DEBUG_BACKTRACE_PROVIDE_OBJECT`** | За замовчуванням. |
| **`DEBUG_BACKTRACE_IGNORE_ARGS`** | Не включати інформацію про аргументи функцій у стеку дзвінків. |

### Значення, що повертаються

Повертає трасування запущеного генератора.

### Приклади

**Приклад #1 Приклад використання** ReflectionGenerator::getTrace()\*\*\*\*

```php
<?php
function foo() {
    yield 1;
}

function bar()
{
    yield from foo();
}

function baz()
{
    yield from bar();
}

$gen = baz();
$gen->valid(); // запускаем генератор

var_dump((new ReflectionGenerator($gen))->getTrace());
```

Висновок наведеного прикладу буде схожим на:

```
array(2) {
  [0]=>
  array(4) {
    ["file"]=>
    string(18) "example.php"
    ["line"]=>
    int(8)
    ["function"]=>
    string(3) "foo"
    ["args"]=>
    array(0) {
    }
  }
  [1]=>
  array(4) {
    ["file"]=>
    string(18) "example.php"
    ["line"]=>
    int(12)
    ["function"]=>
    string(3) "bar"
    ["args"]=>
    array(0) {
    }
  }
}
```

### Дивіться також

-   [ReflectionGenerator::getFunction()](reflectiongenerator.getfunction.md) \- Отримати ім'я функції генератора
-   [ReflectionGenerator::getThis()](reflectiongenerator.getthis.md) \- Отримує значення $this генератора
