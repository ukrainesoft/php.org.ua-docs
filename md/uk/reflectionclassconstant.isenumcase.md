---
navigation:
  - reflectionclassconstant.getvalue.md: '« ReflectionClassConstant::getValue'
  - reflectionclassconstant.isfinal.md: 'ReflectionClassConstant::isFinal »'
  - index.md: PHP Manual
  - class.reflectionclassconstant.md: ReflectionClassConstant
title: 'ReflectionClassConstant::isEnumCase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClassConstant::isEnumCase

(PHP 8 >= 8.1.0)

ReflectionClassConstant::isEnumCase — Перевіряє, чи є константа класу варіантом перерахування

### Опис

```methodsynopsis
public ReflectionClassConstant::isEnumCase(): bool
```

Перевіряє, чи є константа класу варіантом [перерахування](language.enumerations.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*якщо константа класу є варіантом перерахування, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** ReflectionClassConstant::isEnumCase()\*\*\*\*

Визначення варіанта перерахування та звичайної константи класу.

```php
<?php
enum Status
{
    const BORING_CONSTANT = 'test';
    const ENUM_VALUE = Status::PUBLISHED;

    case DRAFT;
    case PUBLISHED;
    case ARCHIVED;
}

$reflection = new ReflectionEnum(Status::class);
foreach ($reflection->getReflectionConstants() as $constant) {
    echo "{$constant->name} - это ",
        $constant->isEnumCase() ? "вариант переключения" : "обычная константа класса",
        PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
BORING_CONSTANT - это обычная константа класса
ENUM_VALUE - это обычная константа класса
DRAFT - это вариант переключения
PUBLISHED - это вариант переключения
ARCHIVED - это вариант переключения
```

### Дивіться також

-   [ReflectionEnum](class.reflectionenum.md)
