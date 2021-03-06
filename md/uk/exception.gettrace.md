- [« Exception::getLine](exception.getline.md)
- [Exception::getTraceAsString »](exception.gettraceasstring.md)

- [PHP Manual](index.md)
- [Exception](class.exception.md)
- Отримує трасування стека

# Exception::getTrace

(PHP 5, PHP 7, PHP 8)

Exception::getTrace — Отримує трасування стека

### Опис

final public **Exception::getTrace**(): array

Повертає трасування стека виключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає трасування стека виключення як масиву (array).

### Приклади

**Приклад #1 Приклад використання **Exception::getTrace()****

` <?phpfunction test() { throw new Exception;}try { test();} catch(Exception $e) { var_dump($e->getTrace());}?> `

Результатом виконання цього прикладу буде щось подібне:

array(1) {
[0]=>
array(4) {
["file"]=>
string(22) "/home/bjori/tmp/ex.php"
["line"]=>
int(7)
["function"]=>
string(4) "test"
["args"]=>
array(0) {
}
}
}

### Дивіться також

- [Throwable::getTrace()](throwable.gettrace.md) - Повертає
трасування стеку
