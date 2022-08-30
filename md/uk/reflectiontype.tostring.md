Перетворення на рядок

-   [« ReflectionType::allowsNull](reflectiontype.allowsnull.md)
    
-   [ReflectionUnionType »](class.reflectionuniontype.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionType](class.reflectiontype.md)
    
-   Перетворення на рядок
    

# ReflectionType::function toString() { \[native code\] }

(PHP 7, PHP 8)

ReflectionType::toString — Перетворення на рядок

**Увага**

Ця функція оголошена *застарілої*починаючи з PHP 7.1.0. Використовувати цю функцію вкрай не рекомендується.

### Опис

```methodsynopsis
public ReflectionType::__toString(): string
```

Отримує назву типу параметра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тип параметра.

### список змін

| Версия | Описание                                             |
|--------|------------------------------------------------------|
|        | **ReflectionType::toString()** оголошено застарілим. |

### Приклади

**Приклад #1 Приклад використання **ReflectionType::toString()****

```php
<?php
function someFunction(string $param) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParam = $reflectionFunc->getParameters()[0];

echo $reflectionParam->getType();
```

Результатом виконання цього прикладу буде щось подібне:

```
string
```

### Дивіться також

-   [ReflectionNamedType::getName()](reflectionnamedtype.getname.md) - Отримує ім'я типу у вигляді рядка
-   [ReflectionNamedType::isBuiltin()](reflectionnamedtype.isbuiltin.md) - Перевіряє, чи є тип вбудованим
-   [ReflectionType::allowsNull()](reflectiontype.allowsnull.md) - Перевіряє, чи допустимо NULL
-   [ReflectionUnionType::getTypes()](reflectionuniontype.gettypes.md) - Повертає типи, включені до типу union
-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) - Отримати тип параметра