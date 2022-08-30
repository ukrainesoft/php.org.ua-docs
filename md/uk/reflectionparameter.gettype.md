Отримати тип параметра

-   [« ReflectionParameter::getPosition](reflectionparameter.getposition.html)
    
-   [ReflectionParameter::hasType »](reflectionparameter.hastype.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionParameter](class.reflectionparameter.html)
    
-   Отримати тип параметра
    

# ReflectionParameter::getType

(PHP 7, PHP 8)

ReflectionParameter::getType — Отримати тип параметра

### Опис

```methodsynopsis
public ReflectionParameter::getType(): ?ReflectionType
```

Отримати тип параметра

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [ReflectionType](class.reflectiontype.html), якщо тип параметра заданий, **`null`**, в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ReflectionParameter::getType()** починаючи з PHP 7.1.0**

Починаючи з PHP 7.1.0, метод [ReflectionType::toString()](reflectiontype.tostring.html) оголошено застарілим. Метод **ReflectionParameter::getType()** *може* повернути екземпляр [ReflectionNamedType](class.reflectionnamedtype.html). Для отримання імені типу параметра доступний метод **ReflectionNamedType()**

```php
<?php
function someFunction(int $param, $param2) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();
$reflectionType1 = $reflectionParams[0]->getType();
$reflectionType2 = $reflectionParams[1]->getType();

assert($reflectionType1 instanceof ReflectionNamedType);
echo $reflectionType1->getName(), PHP_EOL;
var_dump($reflectionType2);
?>
```

Результат виконання цього прикладу:

```
int
NULL
```

**Приклад #2 Використання **ReflectionParameter::getType()** у PHP до версії 7.1.0**

```php
<?php
function someFunction(int $param, $param2) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();
$reflectionType1 = $reflectionParams[0]->getType();
$reflectionType2 = $reflectionParams[1]->getType();

echo $reflectionType1, PHP_EOL;
var_dump($reflectionType2);
?>
```

Результат виконання цього прикладу в PHP 7.0:

```
int
NULL
```

**Приклад #3 Приклад використання **ReflectionParameter::getType()** в PHP 8.0.0 і пізніших**

Починаючи з PHP 8.0.0, цей метод може повертати екземпляр [ReflectionNamedType](class.reflectionnamedtype.html) або екземпляр [ReflectionUnionType](class.reflectionuniontype.html). Останній є колекцією перших. Для аналізу типу часто буває зручно перетворити його на масив об'єктів [ReflectionNamedType](class.reflectionnamedtype.html). Наступна функція поверне масив з `0` або більше екземплярів [ReflectionNamedType](class.reflectionnamedtype.html)

```php
<?php
function getAllTypes(ReflectionParameter $reflectionParameter): array
{
    $reflectionType = $reflectionParameter->getType();

    if (!$reflectionType) return [];

    return $reflectionType instanceof ReflectionUnionType
        ? $reflectionType->getTypes()
        : [$reflectionType];
}
?>
```

### Дивіться також

-   [ReflectionParameter::hasType()](reflectionparameter.hastype.html) - Перевірити, чи вказано тип параметра
-   [ReflectionType::toString()](reflectiontype.tostring.html) - Перетворення на рядок