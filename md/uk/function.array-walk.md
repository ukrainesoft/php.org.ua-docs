Застосовує задану користувачем функцію кожного елемента масиву

-   [« arraywalkrecursive](function.array-walk-recursive.html)
    
-   [array »](function.array.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з масивами](ref.array.html)
    
-   Застосовує задану користувачем функцію кожного елемента масиву
    

# arraywalk

(PHP 4, PHP 5, PHP 7, PHP 8)

arraywalk — Застосовує задану користувачем функцію кожного елемента масиву

### Опис

```methodsynopsis
array_walk(array|object &$array, callable $callback, mixed $arg = null): bool
```

Застосовує функцію користувача `callback` до кожного елементу масиву `array`

**arraywalk()** не схильна до впливу внутрішнього покажчика масиву `array`. . **arraywalk()** обійде всі елементи масиву незалежно від позиції покажчика.

### Список параметрів

`array`

Вхідний масив

`callback`

Зазвичай функція `callback` приймає два параметри. Як перший параметр йде значення елемента масиву `array`, а ключ - як другий.

> **Зауваження**
> 
> Якщо потрібно, щоб функція `callback` змінила значення у масиві, визначте перший параметр `callback` як [ссылку](language.references.html). Тоді всі зміни будуть застосовані до елементів оригінального масиву.

> **Зауваження**
> 
> Багато вбудованих функцій (наприклад, [strtolower()](function.strtolower.html)) виводять попередження, якщо їм передано більше параметрів, ніж вони очікують, або які не можуть безпосередньо використовуватись у `callback`

Потенційно змінені можуть бути лише значення масиву `array`; структура масиву може бути змінена, тобто не можна додати, видалити чи змінити порядок елементів. Якщо callback-функція не відповідає цій вимогі, поведінка цієї функції стане невизначеною і непередбачуваною.

`arg`

Якщо вказано необов'язковий параметр `arg`, він буде переданий як третій параметр в callback-функцію `callback`

### Значення, що повертаються

Повертає **`true`**

### Помилки

Починаючи з PHP 7.1.0, якщо `callback`функція вимагає більше двох параметрів (значення та ключ елемента масиву) або більше 3 параметрів, якщо також передається параметр `arg`, буде викинуто виняток [ArgumentCountError](class.argumentcounterror.html). Раніше в такому разі при кожному виклику `callback`, генерувалася помилка рівня [ЕWARNING](errorfunc.constants.html)

### список змін

| Версия | Описание                                                                                                                                                    |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Якщо параметр `callback` очікує, що значення другого чи третього параметра буде передано за посиланням, функція тепер видасть помилку рівня **`E_WARNING`** |

### Приклади

**Приклад #1 Приклад використання **arraywalk()****

```php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");

function test_alter(&$item1, $key, $prefix)
{
    $item1 = "$prefix: $item1";
}

function test_print($item2, $key)
{
    echo "$key. $item2\n";
}

echo "До ...:\n";
array_walk($fruits, 'test_print');

array_walk($fruits, 'test_alter', 'fruit');
echo "... и после:\n";

array_walk($fruits, 'test_print');
?>
```

Результат виконання цього прикладу:

```
До ...:
d. lemon
a. orange
b. banana
c. apple
... и после:
d. fruit: lemon
a. fruit: orange
b. fruit: banana
c. fruit: apple
```

**Приклад #2 Приклад використання **arraywalk()** з анонімною функцією**

```php
<?php
$elements = ['a', 'b', 'c'];

array_walk($elements, function ($value, $key) {
  echo "{$key} => {$value}\n";
});

?>
```

Результат виконання цього прикладу:

```
0 => a
1 => b
2 => c
```

### Дивіться також

-   [arraywalkrecursive()](function.array-walk-recursive.html) - Рекурсивно застосовує функцію користувача до кожного елементу масиву
-   [iteratorapply()](function.iterator-apply.html) - Викликає функцію кожного елемента в итераторе
-   [list()](function.list.html) - Надає змінним зі списку значення подібно до масиву
-   [each()](function.each.html) - Повертає поточну пару ключ/значення з масиву та зміщує його покажчик
-   [calluserfuncarray()](function.call-user-func-array.html) - Викликає callback-функцію з масивом параметрів
-   [arraymap()](function.array-map.html) - Застосовує callback-функцію до всіх елементів зазначених масивів
-   [foreach](control-structures.foreach.html)