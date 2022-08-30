Отримує об'єкт ReflectionClass для параметра, що відображається, або null

-   [« ReflectionParameter::getAttributes](reflectionparameter.getattributes.html)
    
-   [ReflectionParameter::getDeclaringClass »](reflectionparameter.getdeclaringclass.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionParameter](class.reflectionparameter.html)
    
-   Отримує об'єкт ReflectionClass для параметра, що відображається, або null
    

# ReflectionParameter::getClass

(PHP 5, PHP 7, PHP 8)

ReflectionParameter::getClass — Отримує об'єкт [ReflectionClass](class.reflectionclass.html) для відображуваного параметра або **`null`**

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
public ReflectionParameter::getClass(): ?ReflectionClass
```

Отримує об'єкт [ReflectionClass](class.reflectionclass.html) для відображуваного параметра або **`null`**

Починаючи з PHP 8.0.0, ця функція застаріла і не рекомендується. Замість неї використовуйте [ReflectionParameter::getType()](reflectionparameter.gettype.html), Щоб отримати [ReflectionType](class.reflectiontype.html) параметра, а потім опитайте об'єкт, щоб визначити тип параметра.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт класу [ReflectionClass](class.reflectionclass.html) або \*\*`null`\*\*якщо тип не оголошений або якщо оголошений тип не є класом або інтерфейсом.

### Приклади

**Приклад #1 Приклад використання класу [ReflectionParameter](class.reflectionparameter.html)**

```php
<?php
function foo(Exception $a) { }

$functionReflection = new ReflectionFunction('foo');
$parameters = $functionReflection->getParameters();
$aParameter = $parameters[0];

echo $aParameter->getClass()->name;
?>
```

### Дивіться також

-   [ReflectionParameter::getDeclaringClass()](reflectionparameter.getdeclaringclass.html) - Отримання класу, що оголошує