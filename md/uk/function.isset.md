---
navigation:
  - function.is-string.md: « isstring
  - function.print-r.md: printr »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: isset
---
# isset

(PHP 4, PHP 5, PHP 7, PHP 8)

isset — Визначає, чи була встановлена ​​змінна значенням, відмінним від **`null`**

### Опис

```methodsynopsis
isset(mixed $var, mixed ...$vars): bool
```

Визначає, чи була встановлена ​​змінна значенням відмінним від **`null`**

Якщо змінна була видалена за допомогою [unset()](function.unset.md), то вона більше не вважається за встановлену.

**isset()** поверне **`false`** при перевірці змінної, яка була встановлена ​​значенням **`null`**. Також врахуйте, що NULL-символ (`"\0"`) не дорівнює константі **`null`** у PHP.

Якщо було передано кілька параметрів, то **isset()** поверне **`true`** тільки в тому випадку, якщо визначено всі параметри. Перевірка відбувається зліва направо і закінчується, як тільки зустрінеться невизначена змінна.

### Список параметрів

`var`

Перевірена змінна.

`vars`

Наступні змінні.

### Значення, що повертаються

Повертає **`true`**, якщо `var` визначено та її значення на відміну від **`null`**, і **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **isset()****

```php
<?php

$var = '';

// Проверка вернёт TRUE, поэтому текст будет напечатан.
if (isset($var)) {
    echo "Эта переменная определена, поэтому меня и напечатали.";
}

// В следующем примере мы используем var_dump для вывода
// значения, возвращаемого isset().

$a = "test";
$b = "anothertest";

var_dump(isset($a));     // TRUE
var_dump(isset($a, $b)); // TRUE

unset ($a);

var_dump(isset($a));     // FALSE
var_dump(isset($a, $b)); // FALSE

$foo = NULL;
var_dump(isset($foo));   // FALSE

?>
```

Функція також працює з елементами масивів:

```php
<?php

$a = array ('test' => 1, 'hello' => NULL, 'pie' => array('a' => 'apple'));

var_dump(isset($a['test']));            // TRUE
var_dump(isset($a['foo']));             // FALSE
var_dump(isset($a['hello']));           // FALSE

// Элемент с ключом 'hello' равен NULL, поэтому он считается неопределённым
// Если вы хотите проверить существование ключей со значением NULL, попробуйте так:
var_dump(array_key_exists('hello', $a)); // TRUE

// Проверка вложенных элементов Масива
var_dump(isset($a['pie']['a']));        // TRUE
var_dump(isset($a['pie']['b']));        // FALSE
var_dump(isset($a['cake']['a']['b']));  // FALSE

?>
```

**Приклад #2 **isset()** та рядкові індекси**

```php
<?php
$expected_array_got_string = 'somestring';
var_dump(isset($expected_array_got_string['some_key']));
var_dump(isset($expected_array_got_string[0]));
var_dump(isset($expected_array_got_string['0']));
var_dump(isset($expected_array_got_string[0.5]));
var_dump(isset($expected_array_got_string['0.5']));
var_dump(isset($expected_array_got_string['0 Mostel']));
?>
```

Результат виконання цього прикладу:

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

**isset()** працює тільки зі змінними, тому передача як параметри будь-яких інших значень приведе до помилки парсингу. Для перевірки визначення [констант](language.constants.md) використовуйте функцію [defined()](function.defined.md)

> **Зауваження**: Оскільки це мовна конструкція, а не функція, вона не може викликатися за допомогою [змінних функцій](functions.variable-functions.md) або [іменованих аргументів](functions.arguments.md#functions.named-arguments)

> **Зауваження**
> 
> При використанні **isset()** на недоступних властивостях об'єкта, буде викликатись перевантажений метод [isset()](language.oop5.overloading.md#object.isset)якщо він існує.

### Дивіться також

-   [empty()](function.empty.md) - Перевіряє, чи порожня змінна
-   [isset()](language.oop5.overloading.md#object.isset)
-   [unset()](function.unset.md) - Видаляє змінну
-   [defined()](function.defined.md) - Перевіряє існування вказаної іменованої константи
-   [Таблица сравнения типов](types.comparisons.md)
-   [arraykeyexists()](function.array-key-exists.md) - Перевіряє, чи присутній у масиві зазначений ключ чи індекс
-   [ісnull()](function.is-null.md) - Перевіряє, чи значення змінної дорівнює null
-   Оператор керування помилками[](language.operators.errorcontrol.md)
