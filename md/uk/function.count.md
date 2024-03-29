---
navigation:
  - function.compact.md: « compact
  - function.current.md: current »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Якщо необов'язковий параметр `mode`установлен в\*\*`COUNT_RECURSIVE`\*\*(или 1),**count()** рекурсивно підраховуватиме кількість елементів масиву. Це особливо корисно для підрахунку всіх елементів багатовимірних масивів.

**Застереження**

**count()** вміє визначати рекурсію для уникнення нескінченного циклу, але при кожному виявленні виводить помилку рівня **`E_WARNING`** (у випадку, якщо масив містить більше одного разу) і повертає більшу кількість, ніж могло б очікуватися.

### Значення, що повертаються

Повертає кількість елементів у `value`. До PHP 8.0.0, якщо параметр не був масивом (array), ні об'єктом (object), що реалізує інтерфейс [Countable](class.countable.md), поверталося , если значение параметра`value` не було **`null`**, у цьому випадку поверталося

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | **count()** тепер викидає [TypeError](class.typeerror.md), якщо передано неприпустимий обчислюваний тип параметр `value` |
| 7.2.0 | **count()** тепер видаватиме попередження про неприпустимі обчислювані типи, передані в параметр `value` |

### Приклади

**Приклад #1 Приклад використання** count()\*\*\*\*

```php
<?php
$a[0] = 1;
$a[1] = 3;
$a[2] = 5;
var_dump(count($a));

$b[0]  = 7;
$b[5]  = 9;
$b[10] = 11;
var_dump(count($b));
?>
```

Результат виконання наведеного прикладу:

```
int(3)
int(3)
```

**Приклад #2 Приклад використання** count()\*\* з незліченним типом (поганий приклад - не робіть так)\*\*

```php
<?php
$b[0]  = 7;
$b[5]  = 9;
$b[10] = 11;
var_dump(count($b));

var_dump(count(null));

var_dump(count(false));
?>
```

Результат виконання наведеного прикладу:

```
int(3)
int(0)
int(1)
```

Результат виконання наведеного прикладу в PHP 7.2:

```
int(3)

Warning: count(): Parameter must be an array or an object that implements Countable in … on line 12
int(0)

Warning: count(): Parameter must be an array or an object that implements Countable in … on line 14
int(1)
```

Результат виконання наведеного прикладу в PHP 8:

```
int(3)

Fatal error: Uncaught TypeError: count(): Argument #1 ($var) must be of type Countable .. on line 12
```

**Приклад #3 Приклад рекурсивного використання **count()****

```php
<?php
$food = array('fruits' => array('orange', 'banana', 'apple'),
              'veggie' => array('carrot', 'collard', 'pea'));

// рекурсивный подсчёт
var_dump(count($food, COUNT_RECURSIVE));

// обычный подсчёт
var_dump(count($food));

?>
```

Результат виконання наведеного прикладу:

```
int(8)
int(2)
```

**Приклад #4 Об'єкт, що реалізує інтерфейс [Countable](class.countable.md)**

```php
<?php
class CountOfMethods implements Countable
{
    private function someMethod()
    {
    }

    public function count(): int
    {
        return count(get_class_methods($this));
    }
}

$obj = new CountOfMethods();
var_dump(count($obj));
?>
```

Результат виконання наведеного прикладу:

```
int(2)
```

### Дивіться також

-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
-   [isset()](function.isset.md) \- Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [empty()](function.empty.md) \- Перевіряє, чи порожня змінна
-   [strlen()](function.strlen.md) \- Повертає довжину рядка
-   [is\_countable()](function.is-countable.md) \- Перевіряє, чи є зміст змінної лічильне значення
-   [Масиви](language.types.array.md)
