Отримання імен класів

-   [« ReflectionExtension::getClasses](reflectionextension.getclasses.md)
    
-   [ReflectionExtension::getConstants »](reflectionextension.getconstants.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionExtension](class.reflectionextension.md)
    
-   Отримання імен класів
    

# ReflectionExtension::getClassNames

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getClassNames — Отримання імен класів

### Опис

```methodsynopsis
public ReflectionExtension::getClassNames(): array
```

Отримує список імен класів, як визначено в модулі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) імен класів, визначених у модулі. Якщо жодних класів не визначено, буде повернено порожній масив.

### Приклади

**Приклад #1 Приклад використання **ReflectionExtension::getClassNames()****

```php
<?php
$ext = new ReflectionExtension('XMLWriter');
var_dump($ext->getClassNames());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [0]=>
  string(9) "XMLWriter"
}
```

### Дивіться також

-   [ReflectionExtension::getClasses()](reflectionextension.getclasses.md) - Повертає класи
-   [ReflectionExtension::getName()](reflectionextension.getname.md) - Отримання імені модуля