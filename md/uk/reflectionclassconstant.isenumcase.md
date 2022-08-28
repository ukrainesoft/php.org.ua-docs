Перевіряє, чи є константа класу варіантом перерахування

-   [« ReflectionClassConstant::getValue](reflectionclassconstant.getvalue.html)
    
-   [ReflectionClassConstant::isFinal »](reflectionclassconstant.isfinal.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClassConstant](class.reflectionclassconstant.html)
    
-   Перевіряє, чи є константа класу варіантом перерахування
    

# ReflectionClassConstant::isEnumCase

(PHP 8> = 8.1.0)

ReflectionClassConstant::isEnumCase — Перевіряє, чи є константа класу варіантом перерахування

### Опис

```methodsynopsis
public ReflectionClassConstant::isEnumCase(): bool
```

Перевіряє, чи є константа класу варіантом [перечисления](language.enumerations.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає **`true`**якщо константа класу є варіантом перерахування, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionClassConstant::isEnumCase()****

Визначення варіанта перерахування та звичайної константи класу.

```php
<?php
enum Status
{
    const BORING_CONSTANT = 'test';
    const ENUM_VALUE = Status::PUBLISHED;

    case DRAFT;
    case PUBLISHED;
    case ARCHIVED;
}

$reflection = new ReflectionEnum(Status::class);
foreach ($reflection->getReflectionConstants() as $constant) {
    echo "{$constant->name} - это ",
        $constant->isEnumCase() ? "вариант переключения" : "обычная константа класса",
        PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
BORING_CONSTANT - это обычная константа класса
ENUM_VALUE - это обычная константа класса
DRAFT - это вариант переключения
PUBLISHED - это вариант переключения
ARCHIVED - это вариант переключения
```

### Дивіться також

-   [ReflectionEnum](class.reflectionenum.html)