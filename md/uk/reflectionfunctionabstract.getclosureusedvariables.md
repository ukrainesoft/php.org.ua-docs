- [« ReflectionFunctionAbstract::getClosureThis](reflectionfunctionabstract.getclosurethis.md)
- [ReflectionFunctionAbstract::getDocComment »](reflectionfunctionabstract.getdoccomment.md)

- [PHP Manual](index.md)
- [ReflectionFunctionAbstract](class.reflectionfunctionabstract.md)
- Повертає масив змінних, що використовуються в замиканні.

# ReflectionFunctionAbstract::getClosureUsedVariables

(PHP 8 \>= 8.1.0)

ReflectionFunctionAbstract::getClosureUsedVariables — Повертає масив
використовуваних у замиканні змінних

### Опис

public **ReflectionFunctionAbstract::getClosureUsedVariables**(): array

Повертає масив (array), що використовуються в [Closure](class.closure.md)
змінних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що використовуються в [Closure](class.closure.md)
змінних.

### Приклади

**Приклад #1 Приклад використання
**ReflectionFunctionAbstract::getClosureUsedVariables()****

` <?php$one = 1;$two = 2;$function = function() use ($one, $two) {    static $three = 3;};$reflector==new ReflectionFun$ reflector->getClosureUsedVariables());?> `

Результатом виконання цього прикладу буде щось подібне:

array(2) {
["one"]=>
int(1)
["two"]=>
int(2)
}

### Дивіться також

- [ReflectionFunctionAbstract::getClosureScopeClass()](reflectionfunctionabstract.getclosurescopeclass.md) -
Повертає клас, в рамках якого було оголошено замикання
- [ReflectionFunctionAbstract::getClosureThis()](reflectionfunctionabstract.getclosurethis.md) -
Повертає вказівник, прив'язаний до замикання
