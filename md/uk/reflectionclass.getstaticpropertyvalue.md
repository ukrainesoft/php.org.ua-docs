Повертає значення статичної властивості

-   [« ReflectionClass::getStaticProperties](reflectionclass.getstaticproperties.md)
    
-   [ReflectionClass::getTraitAliases »](reflectionclass.gettraitaliases.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionClass](class.reflectionclass.md)
    
-   Повертає значення статичної властивості
    

# ReflectionClass::getStaticPropertyValue

(PHP 5> = 5.1.2, PHP 7, PHP 8)

ReflectionClass::getStaticPropertyValue — Повертає значення статичної властивості

### Опис

```methodsynopsis
public ReflectionClass::getStaticPropertyValue(string $name, mixed &$def_value = ?): mixed
```

Повертає значення статичної якості класу.

### Список параметрів

`name`

Ім'я статичної властивості, значення якої необхідно отримати

`def_value`

Значення за умовчанням, що повертається у випадку, якщо в класі не визначено статичну властивість із заданим ім'ям `name`. Якщо властивість немає і цей аргумент не заданий, то викидається [ReflectionException](class.reflectionexception.md)

### Значення, що повертаються

Значення статичної якості.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getStaticPropertyValue()****

```php
<?php
class Apple {
    public static $color = 'Red';
}

$class = new ReflectionClass('Apple');
var_dump($class->getStaticPropertyValue('color'));
?>
```

Результат виконання цього прикладу:

```
string(3) "Red"
```

### Дивіться також

-   [ReflectionClass::getStaticProperties()](reflectionclass.getstaticproperties.md) - Повертає статичні властивості
-   [ReflectionClass::setStaticPropertyValue()](reflectionclass.setstaticpropertyvalue.md) - Встановлює значення статичної властивості