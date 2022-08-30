Підраховує кількість елементів масиву або Countable об'єкті

-   [« compact](function.compact.md)
    
-   [current »](function.current.md)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з масивами](ref.array.md)
    
-   Підраховує кількість елементів масиву або Countable об'єкті
    

# count

(PHP 4, PHP 5, PHP 7, PHP 8)

count — Підраховує кількість елементів масиву або [Countable](class.countable.md) об'єкті

### Опис

```methodsynopsis
count(Countable|array $value, int $mode = COUNT_NORMAL): int
```

Підраховує всі елементи у масиві, якщо використовується масив. Якщо використовується об'єкт, який реалізує інтерфейс [Countable](class.countable.md), функція повертає результат виконання методу [Countable::count()](countable.count.md)

### Список параметрів

`value`

Масив чи об'єкт, що реалізує [Countable](class.countable.md)

`mode`

Якщо необов'язковий параметр `mode` встановлений в **`COUNT_RECURSIVE`** (або 1), **count()** рекурсивно підраховуватиме кількість елементів масиву. Це особливо корисно для підрахунку всіх елементів багатовимірних масивів.

**Застереження**

**count()** вміє визначати рекурсію для уникнення нескінченного циклу, але при кожному виявленні виводить помилку рівня **`E_WARNING`** (якщо масив містить себе більше одного разу) і повертає більшу кількість, ніж могло б очікуватися.

### Значення, що повертаються

Повертає кількість елементів у `value`. До PHP 8.0.0, якщо параметр не був масивом (array), ні об'єктом (object), що реалізує інтерфейс [Countable](class.countable.md), поверталося `1`, якщо значення параметра `value` не було **`null`**, у цьому випадку поверталося `0`

### список змін

| Версия | Описание                                                                                                                 |
|--------|--------------------------------------------------------------------------------------------------------------------------|
|        | **count()** тепер викидає [TypeError](class.typeerror.md), якщо передано неприпустимий обчислюваний тип параметр `value` |
|        | **count()** тепер буде видавати попередження про неприпустимі обчислювані типи, передані в параметр `value`              |

### Приклади

**Приклад #1 Приклад використання **count()****

```php
<?php
$a[0] = 1;
$a[1] = 3;
$a[2] = 5;
var_dump(count($a));

$b[0]  = 7;
$b[5]  = 9;
$b[10] = 11;
var_dump(count($b));
?>
```

Результат виконання цього прикладу:

```
int(3)
int(3)
```

**Приклад #2 Приклад використання **count()** з незліченним типом (поганий приклад - не робіть так)**

```php
<?php
$b[0]  = 7;
$b[5]  = 9;
$b[10] = 11;
var_dump(count($b));

var_dump(count(null));

var_dump(count(false));
?>
```

Результат виконання цього прикладу:

```
int(3)
int(0)
int(1)
```

Результат виконання цього прикладу в PHP 7.2:

```
int(3)

Warning: count(): Parameter must be an array or an object that implements Countable in … on line 12
int(0)

Warning: count(): Parameter must be an array or an object that implements Countable in … on line 14
int(1)
```

Результат виконання цього прикладу в PHP 8:

```
int(3)

Fatal error: Uncaught TypeError: count(): Argument #1 ($var) must be of type Countable .. on line 12
```

**Приклад #3 Приклад рекурсивного використання **count()****

```php
<?php
$food = array('fruits' => array('orange', 'banana', 'apple'),
              'veggie' => array('carrot', 'collard', 'pea'));

// рекурсивный подсчёт
var_dump(count($food, COUNT_RECURSIVE));

// обычный подсчёт
var_dump(count($food));

?>
```

Результат виконання цього прикладу:

```
int(8)
int(2)
```

**Приклад #4 Об'єкт, що реалізує інтерфейс [Countable](class.countable.md)**

```php
<?php
class CountOfMethods implements Countable
{
    private function someMethod()
    {
    }

    public function count(): int
    {
        return count(get_class_methods($this));
    }
}

$obj = new CountOfMethods();
var_dump(count($obj));
?>
```

Результат виконання цього прикладу:

```
int(2)
```

### Дивіться також

-   [ісarray()](function.is-array.html) - Визначає, чи є змінна масивом
-   [isset()](function.isset.md) - Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [empty()](function.empty.md) - Перевіряє, чи порожня змінна
-   [strlen()](function.strlen.md) - Повертає довжину рядка
-   [ісcountable()](function.is-countable.html) - Перевірити, що вміст змінної є лічильним значенням
-   [Масиви](language.types.array.md)