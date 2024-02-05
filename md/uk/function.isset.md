---
navigation:
  - function.is-string.md: « is\_string
  - function.print-r.md: print\_r »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: isset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# isset

(PHP 4, PHP 5, PHP 7, PHP 8)

isset — Визначає, чи була встановлена ​​змінна значенням, відмінним від **`null`**

### Опис

```methodsynopsis
isset(mixed $var, mixed ...$vars): bool
```

Визначає, чи була встановлена ​​змінна значенням, відмінним від **`null`**

Якщо змінну було видалено через мовну конструкцію [unset()](function.unset.md)то змінна більше не вважається встановленою.

Мовна конструкція **isset()** поверне **`false`** під час перевірки змінної, для якої було встановлено значення **`null`**. Врахуйте також, що NULL-символ (`«\0»`) не равен константе\*\*`null`\*\* у PHP.

Якщо було передано кілька параметрів, то конструкція **isset()** поверне **`true`** тільки тоді, коли визначено всі параметри. Перевірка виконується зліва направо і закінчується, як тільки зустрінеться невизначена змінна.

### Список параметрів

`var`

Перевірена змінна.

`vars`

Наступні змінні.

### Значення, що повертаються

Повертає **`true`**, якщо передана у параметр `var` змінна визначена і її значення відрізняється від **`null`**. В інших випадках повертає **`false`**

### Приклади

**Приклад #1 Приклад використання мовної конструкції **isset()****

```php
<?php

$var = '';

// Проверка вернёт TRUE, поэтому текст будет напечатан.
if (isset($var)) {
    echo "Эта переменная определена, поэтому меня и напечатали.";
}

// В следующем примере вызывается функция var_dump для вывода
// значения, возвращаемого конструкцией isset().

$a = "test";
$b = "anothertest";

var_dump(isset($a));     // TRUE
var_dump(isset($a, $b)); // TRUE

unset ($a);

var_dump(isset($a));     // FALSE
var_dump(isset($a, $b)); // FALSE

$foo = NULL;
var_dump(isset($foo));   // FALSE

?>
```

Конструкція також працює з елементами масивів:

```php
<?php

$a = array ('test' => 1, 'hello' => NULL, 'pie' => array('a' => 'apple'));

var_dump(isset($a['test']));            // TRUE
var_dump(isset($a['foo']));             // FALSE
var_dump(isset($a['hello']));           // FALSE

// Элемент с ключом «hello» равен NULL, поэтому он считается неопределённым
// Если нужно проверить существование ключей со значением NULL, делают так:
var_dump(array_key_exists('hello', $a)); // TRUE

// Проверка вложенных элементов массива
var_dump(isset($a['pie']['a']));        // TRUE
var_dump(isset($a['pie']['b']));        // FALSE
var_dump(isset($a['cake']['a']['b']));  // FALSE

?>
```

**Приклад #2 Мовна конструкція **isset()** та рядкові індекси**

```php
<?php
$expected_array_got_string = 'somestring';
var_dump(isset($expected_array_got_string['some_key']));
var_dump(isset($expected_array_got_string[0]));
var_dump(isset($expected_array_got_string['0']));
var_dump(isset($expected_array_got_string[0.5]));
var_dump(isset($expected_array_got_string['0.5']));
var_dump(isset($expected_array_got_string['0 Mostel']));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)
```

### Примітки

**Увага**

Конструкция**isset()** працює тільки зі змінними, тому передача як аргументи будь-яких інших значень призведе до помилки парсингу. Для перевірки визначення [констант](language.constants.md) користуються функцією [defined()](function.defined.md)

> **Зауваження**: Оскільки це мовна конструкція, а не функція, її не можна викликати як [змінну функцію](functions.variable-functions.md) або передавати як [іменований аргумент](functions.arguments.md#functions.named-arguments)

> **Зауваження** :
> 
> При виклику конструкції **isset()** на недоступних властивостях об'єкта, викликатиметься метод перевантаження [\_\_isset()](language.oop5.overloading.md#object.isset)якщо він існує.

### Дивіться також

-   [empty()](function.empty.md) \- Перевіряє, чи порожня змінна
-   [\_\_isset()](language.oop5.overloading.md#object.isset)
-   [unset()](function.unset.md) \- Видаляє змінну
-   [defined()](function.defined.md) \- Перевіряє існування вказаної іменованої константи
-   [Таблиця порівняння типів](types.comparisons.md)
-   [array\_key\_exists()](function.array-key-exists.md) \- Перевіряє, чи існує в масиві заданий ключ чи індекс
-   [is\_null()](function.is-null.md) \- Перевіряє, чи значення змінної null дорівнює
-   Оператор керування помилками[@](language.operators.errorcontrol.md)
