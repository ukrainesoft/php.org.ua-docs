---
navigation:
  - reflectionparameter.getdeclaringfunction.md: '« ReflectionParameter::getDeclaringFunction'
  - reflectionparameter.getdefaultvalueconstantname.md: 'ReflectionParameter::getDefaultValueConstantName »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::getDefaultValue'
---
# ReflectionParameter::getDefaultValue

(PHP 5> = 5.0.3, PHP 7, PHP 8)

ReflectionParameter::getDefaultValue — Отримання стандартного значення для параметра

### Опис

```methodsynopsis
public ReflectionParameter::getDefaultValue(): mixed
```

Отримує значення за замовчуванням параметра, будь-якого певного користувача або внутрішньої функції або методу. Якщо аргумент не є необов'язковим, буде викинуто виняток [ReflectionException](class.reflectionexception.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення за промовчанням аргументу.

### список змін

| Версия | Описание |
| --- | --- |
|  | Метод тепер дозволяє отримати значення за промовчанням для параметрів вбудованих функцій та вбудованих методів класу. Раніше викидалося [ReflectionException](class.reflectionexception.md) |

### Приклади

**Приклад #1 Отримання**

```php
<?php
function foo($test, $bar = 'baz')
{
    echo $test . $bar;
}

$function = new ReflectionFunction('foo');

foreach ($function->getParameters() as $param) {
    echo 'Имя: ' . $param->getName() . PHP_EOL;
    if ($param->isOptional()) {
        echo 'Значение по умолчанию: ' . $param->getDefaultValue() . PHP_EOL;
    }
    echo PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
Имя: test

Имя: bar
Значение по умолчанию: baz
```

### Дивіться також

-   [ReflectionParameter::isOptional()](reflectionparameter.isoptional.md) - Перевіряє, чи є аргумент необов'язковим
-   [ReflectionParameter::isDefaultValueAvailable()](reflectionparameter.isdefaultvalueavailable.md) - Перевіряє, чи є значення за замовчуванням
-   [ReflectionParameter::getDefaultValueConstantName()](reflectionparameter.getdefaultvalueconstantname.md) - Повертає ім'я константи значення за промовчанням, якщо значення за промовчанням константа або null
-   [ReflectionParameter::isPassedByReference()](reflectionparameter.ispassedbyreference.md) - Перевіряє, чи передано параметр за посиланням
