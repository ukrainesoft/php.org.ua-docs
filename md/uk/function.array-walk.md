---
navigation:
  - function.array-walk-recursive.md: « array\_walk\_recursive
  - function.array.md: array »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_walk
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_walk

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_walk — Застосовує задану користувачем функцію кожного елемента масиву

### Опис

```methodsynopsis
array_walk(array|object &$array, callable $callback, mixed $arg = null): bool
```

Застосовує функцію користувача `callback` до кожного елементу масиву `array`

**array\_walk()** не схильна до впливу внутрішнього покажчика масиву `array`. . **array\_walk()** обійде всі елементи масиву незалежно від позиції покажчика.

### Список параметрів

`array`

Вхідний масив

`callback`

Зазвичай функція `callback` приймає два параметри. Як перший параметр йде значення елемента масиву `array`, а ключ - як другий.

> **Зауваження** :
> 
> Якщо потрібно, щоб функція `callback` змінила значення у масиві, визначте перший параметр `callback` як [посилання](language.references.md). Тоді всі зміни будуть застосовані до елементів оригінального масиву.

> **Зауваження** :
> 
> Багато вбудованих функцій (наприклад, [strtolower()](function.strtolower.md)) виводять попередження, якщо їм передано більше параметрів, ніж вони очікують, або які не можуть безпосередньо використовуватись у `callback`

Потенційно змінені можуть бути лише значення масиву `array`; структура самого масиву може бути змінена, тобто не можна додати, видалити чи змінити порядок елементів. Якщо callback-функція не відповідає цій вимогі, поведінка цієї функції стане невизначеною і непередбачуваною.

`arg`

Якщо вказано необов'язковий параметр `arg`, він буде переданий як третій параметр в callback-функцію `callback`

### Значення, що повертаються

Повертає **`true`**

### Помилки

Починаючи з PHP 7.1.0, якщо `callback`\-функція вимагає більше двох параметрів (значення та ключ елемента масиву) або більше 3 параметрів, якщо також передається параметр `arg`, буде викинуто виняток [ArgumentCountError](class.argumentcounterror.md). Раніше в такому разі при кожному виклику `callback`, генерувалася помилка рівня [E\_WARNING](errorfunc.constants.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Якщо параметр `callback` очікує, що значення другого чи третього параметра буде передано за посиланням, функція тепер видасть помилку рівня **`E_WARNING`** |

### Приклади

**Приклад #1 Приклад використання** array\_walk()\*\*\*\*

```php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");

function test_alter(&$item1, $key, $prefix)
{
    $item1 = "$prefix: $item1";
}

function test_print($item2, $key)
{
    echo "$key. $item2\n";
}

echo "До ...:\n";
array_walk($fruits, 'test_print');

array_walk($fruits, 'test_alter', 'fruit');
echo "... и после:\n";

array_walk($fruits, 'test_print');
?>
```

Результат виконання наведеного прикладу:

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

**Приклад #2 Приклад використання** array\_walk()\*\* з анонімною функцією\*\*

```php
<?php
$elements = ['a', 'b', 'c'];

array_walk($elements, function ($value, $key) {
  echo "{$key} => {$value}\n";
});

?>
```

Результат виконання наведеного прикладу:

```
0 => a
1 => b
2 => c
```

### Дивіться також

-   [array\_walk\_recursive()](function.array-walk-recursive.md) \- Рекурсивно застосовує функцію користувача до кожного елементу масиву
-   [iterator\_apply()](function.iterator-apply.md) \- Викликає функцію кожного елемента в итераторе
-   [list()](function.list.md) \- надає змінним значення схожим на масиви синтаксисом
-   [each()](function.each.md) \- Повертає поточну пару ключ/значення з масиву та зміщує його покажчик
-   [call\_user\_func\_array()](function.call-user-func-array.md) \- Викликає callback-функцію з масивом параметрів
-   [array\_map()](function.array-map.md) \- Застосовує callback-функцію до всіх елементів зазначених масивів
-   [foreach](control-structures.foreach.md)
