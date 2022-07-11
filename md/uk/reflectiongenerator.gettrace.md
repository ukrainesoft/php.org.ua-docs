- [« ReflectionGenerator::getThis](reflectiongenerator.getthis.md)
- [ReflectionFiber »](class.reflectionfiber.md)

- [PHP Manual](index.md)
- [ReflectionGenerator](class.reflectiongenerator.md)
- Отримати трасування запущеного генератора

# ReflectionGenerator::getTrace

(PHP 7, PHP 8)

ReflectionGenerator::getTrace — Отримати трасування запущеного
генератора

### Опис

public **ReflectionGenerator::getTrace**(int `$options` =
**`DEBUG_BACKTRACE_PROVIDE_OBJECT`**): array

Повертає трасування запущеного генератора.

### Список параметрів

`options`
Значення `options` може бути одним із наступних прапорів:

| Опція                              | Опис                                                           |
| ---------------------------------- | -------------------------------------------------------------- |
| **DEBUG_BACKTRACE_PROVIDE_OBJECT** | За замовчуванням.                                              |                                                                
| **DEBUG_BACKTRACE_IGNORE_ARGS**    | Не включати інформацію про аргументи функцій у стеку дзвінків. |

**Доступні опції**

### Значення, що повертаються

Повертає трасування запущеного генератора.

### Приклади

**Приклад #1 Приклад використання **ReflectionGenerator::getTrace()****

` <?phpfunction foo() {   yield 1;}function bar(){   yield from foo();}function baz(){    yield from bar();}$gen ; // запускаємо генераторvar_dump((new ReflectionGenerator($gen))->getTrace()); `

Результатом виконання цього прикладу буде щось подібне:

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

### Дивіться також

- [ReflectionGenerator::getFunction()](reflectiongenerator.getfunction.md) -
Отримати ім'я функції генератора
- [ReflectionGenerator::getThis()](reflectiongenerator.getthis.md) -
Отримує значення $this генератора
