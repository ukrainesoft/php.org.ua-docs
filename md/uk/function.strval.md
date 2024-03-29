---
navigation:
  - function.settype.md: « settype
  - function.unserialize.md: unserialize »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: strval
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strval

(PHP 4, PHP 5, PHP 7, PHP 8)

strval — Повертає строкове значення змінної

### Опис

```methodsynopsis
strval(mixed $value): string
```

Повертає строкове значення змінної. Дивіться документацію типу string для більш детальної інформації про перетворення в рядок.

Ця функція не робить форматування значення, що повертається. Якщо потрібно привести числове значення до рядка з особливим форматом, скористайтесь [sprintf()](function.sprintf.md) або [number\_format()](function.number-format.md)

### Список параметрів

`value`

Змінна, яку потрібно перетворити на рядок.

`value` може бути будь-якого скалярного типу, null або об'єктом (object), який реалізує метод [\_\_toString()](language.oop5.magic.md#object.tostring). . **strval()** не можна застосувати до масиву або об'єкта, які не реалізують метод [\_\_toString()](language.oop5.magic.md#object.tostring)

### Значення, що повертаються

Строковое значение (string) параметра`value`

### Приклади

**Приклад #1 Приклад використання** strval()\*\* з магічним методом PHP [\_\_toString()](language.oop5.magic.md#object.tostring)\*\*

```php
<?php
class StrValTest
{
    public function __toString()
    {
        return __CLASS__;
    }
}

// Выводит 'StrValTest'
echo strval(new StrValTest);
?>
```

### Дивіться також

-   [boolval()](function.boolval.md) \- Повертає логічне значення змінної
-   [floatval()](function.floatval.md) \- Повертає значення змінної у вигляді числа з плаваючою точкою
-   [intval()](function.intval.md) \- Повертає ціле значення змінної
-   [settype()](function.settype.md) \- Задає тип змінної
-   [sprintf()](function.sprintf.md) \- Повертає відформатований рядок
-   [number\_format()](function.number-format.md) \- Форматує число з поділом груп
-   [Маніпуляції з типами](language.types.type-juggling.md)
-   [\_\_toString()](language.oop5.magic.md#object.tostring)
