Повертає ім'я модуля, що визначає клас

-   [« ReflectionClass::getExtension](reflectionclass.getextension.html)
    
-   [ReflectionClass::getFileName »](reflectionclass.getfilename.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Повертає ім'я модуля, що визначає клас
    

# ReflectionClass::getExtensionName

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getExtensionName — Повертає ім'я модуля, що визначає клас

### Опис

```methodsynopsis
public ReflectionClass::getExtensionName(): string|false
```

Повертає ім'я модуля, який визначає клас.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я модуля, що визначає клас, або **`false`** для класів користувача.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getExtensionName()****

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$extension = $class->getExtensionName();
var_dump($extension);
?>
```

Результат виконання цього прикладу:

```
string(10) "Reflection"
```

### Дивіться також

-   [ReflectionClass::getExtension()](reflectionclass.getextension.html) - Повертає об'єкт класу ReflectionExtension для модуля, що визначає клас