---
navigation:
  - reflectionparameter.getdefaultvalue.md: '« ReflectionParameter::getDefaultValue'
  - reflectionparameter.getname.md: 'ReflectionParameter::getName »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::getDefaultValueConstantName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::getDefaultValueConstantName

(PHP 5 >= 5.4.6, PHP 7, PHP 8)

ReflectionParameter::getDefaultValueConstantName — Повертає ім'я константи значення за промовчанням, якщо значення за промовчанням константа або null

### Опис

```methodsynopsis
public ReflectionParameter::getDefaultValueConstantName(): ?string
```

Повертає значення за промовчанням константи для параметра будь-якої користувальницької чи внутрішньої функції чи методу, якщо значення за промовчанням константа чи null. Якщо параметр необов'язковий, викидається виняток [ReflectionException](class.reflectionexception.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод дозволяє отримувати імена значень за промовчанням для вбудованих функцій та вбудованих методів класу. Раніше викидалося [ReflectionException](class.reflectionexception.md) |

### Приклади

**Приклад #1 Отримання стандартних констант для параметрів функції**

```php
<?php
function foo($test, $bar = PHP_INT_MIN)
{
    echo $test . $bar;
}

$function = new ReflectionFunction('foo');

foreach ($function->getParameters() as $param) {
    echo 'Имя: ' . $param->getName() . PHP_EOL;
    if ($param->isOptional()) {
        echo 'Значение по умолчанию: ' . $param->getDefaultValueConstantName() . PHP_EOL;
    }
    echo PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
Name: test

Имя: bar
Значение по умолчанию: PHP_INT_MIN
```

### Дивіться також

-   [ReflectionParameter::isOptional()](reflectionparameter.isoptional.md) \- Перевіряє, чи є аргумент необов'язковим
-   [ReflectionParameter::isDefaultValueConstant()](reflectionparameter.isdefaultvalueconstant.md) \- Визначити, чи значення параметра за промовчанням константою
-   [ReflectionParameter::getDefaultValue()](reflectionparameter.getdefaultvalue.md) \- Отримання значення за промовчанням для параметра
