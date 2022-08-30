Повертає строкове значення змінної

-   [« settype](function.settype.html)
    
-   [unserialize »](function.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи зі змінними](ref.var.html)
    
-   Повертає строкове значення змінної
    

# strval

(PHP 4, PHP 5, PHP 7, PHP 8)

strval — Повертає строкове значення змінної

### Опис

```methodsynopsis
strval(mixed $value): string
```

Повертає строкове значення змінної. Дивіться документацію типу string для більш детальної інформації про перетворення в рядок.

Ця функція не робить форматування значення, що повертається. Якщо потрібно привести числове значення до рядка з особливим форматом, скористайтесь [sprintf()](function.sprintf.html) або [numberformat()](function.number-format.html)

### Список параметрів

`value`

Змінна, яку потрібно перетворити на рядок.

`value` може бути будь-якого скалярного типу або об'єктом, що реалізує метод [toString()](language.oop5.magic.html#object.tostring). . **strval()** не можна застосувати до масиву або об'єкта, які не реалізують метод [toString()](language.oop5.magic.html#object.tostring)

### Значення, що повертаються

Строкове значення (string) параметра `value`

### Приклади

**Приклад #1 Приклад використання **strval()** з магічним методом PHP [toString()](language.oop5.magic.html#object.tostring)**

```php
<?php
class StrValTest
{
    public function __toString()
    {
        return __CLASS__;
    }
}

// Выводит 'StrValTest'
echo strval(new StrValTest);
?>
```

### Дивіться також

-   [boolval()](function.boolval.html) - Повертає логічне значення змінної
-   [floatval()](function.floatval.html) - Повертає значення змінної у вигляді числа з плаваючою точкою
-   [intval()](function.intval.html) - Повертає ціле значення змінної
-   [settype()](function.settype.html) - Задає тип змінної
-   [sprintf()](function.sprintf.html) - Повертає відформатований рядок
-   [numberformat()](function.number-format.html) - Форматує число з поділом груп
-   [Маніпуляції з типами](language.types.type-juggling.html)
-   [toString()](language.oop5.magic.html#object.tostring)