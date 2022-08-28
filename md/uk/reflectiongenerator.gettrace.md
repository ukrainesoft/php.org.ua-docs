Отримати трасування запущеного генератора

-   [« ReflectionGenerator::getThis](reflectiongenerator.getthis.html)
    
-   [ReflectionFiber »](class.reflectionfiber.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionGenerator](class.reflectiongenerator.html)
    
-   Отримати трасування запущеного генератора
    

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

Значення `options` може бути одним з наступних прапорів:

**Доступні опції**

| Опция                                | Описание                                                       |
|--------------------------------------|----------------------------------------------------------------|
| **`DEBUG_BACKTRACE_PROVIDE_OBJECT`** | За замовчуванням.                                              |
| **`DEBUG_BACKTRACE_IGNORE_ARGS`**    | Не включати інформацію про аргументи функцій у стеку дзвінків. |

### Значення, що повертаються

Повертає трасування запущеного генератора.

### Приклади

**Приклад #1 Приклад використання **ReflectionGenerator::getTrace()****

```php
<?php
function foo() {
    yield 1;
}

function bar()
{
    yield from foo();
}

function baz()
{
    yield from bar();
}

$gen = baz();
$gen->valid(); // запускаем генератор

var_dump((new ReflectionGenerator($gen))->getTrace());
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [ReflectionGenerator::getFunction()](reflectiongenerator.getfunction.html) - Отримати ім'я функції генератора
-   [ReflectionGenerator::getThis()](reflectiongenerator.getthis.html) - Отримує значення $this генератора