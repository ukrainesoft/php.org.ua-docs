- [« ReflectionClass::getInterfaces](reflectionclass.getinterfaces.md)
- [ReflectionClass::getMethods »](reflectionclass.getmethods.md)

- [PHP Manual](index.md)
- [ReflectionClass](class.reflectionclass.md)
- Повертає екземпляр ReflectionMethod для методу класу

# ReflectionClass::getMethod

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getMethod — Повертає екземпляр
[ReflectionMethod](class.reflectionmethod.md) для методу класу

### Опис

public **ReflectionClass::getMethod**(string `$name`):
[ReflectionMethod](class.reflectionmethod.md)

Повертає екземпляр [ReflectionMethod](class.reflectionmethod.md) для
методу класу.

### Список параметрів

`name`
Досліджуваний метод.

### Значення, що повертаються

Примірник класу [ReflectionMethod](class.reflectionmethod.md).

### Помилки

[ReflectionException](class.reflectionexception.md) у випадку, якщо
метод не існує.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getMethod()****

` <?php$class = new ReflectionClass('ReflectionClass');$method = $class->getMethod('getMethod');var_dump($method);?> `

Результат виконання цього прикладу:

object(ReflectionMethod)#2 (2) {
["name"]=>
string(9) "getMethod"
["class"]=>
string(15) "ReflectionClass"
}

### Дивіться також

- [ReflectionClass::getMethods()](reflectionclass.getmethods.md) -
Повертає список методів у вигляді масиву
