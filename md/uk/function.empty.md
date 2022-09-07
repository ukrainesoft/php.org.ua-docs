---
navigation:
  - function.doubleval.md: « doubleval
  - function.floatval.md: floatval »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: empty
---
# empty

(PHP 4, PHP 5, PHP 7, PHP 8)

empty — Перевіряє, чи порожня змінна

### Опис

```methodsynopsis
empty(mixed $var): bool
```

Перевіряє, чи вважається змінна пустою. Змінна вважається порожньою, якщо вона не існує або її значення дорівнює **`false`**. . **empty()** не генерує попередження, якщо змінна немає.

### Список параметрів

`var`

Перевірена змінна

Якщо змінна немає, попередження не генерується. Це означає що **empty()** фактично є точним еквівалентом конструкції **!isset($var) || $var == false**

### Значення, що повертаються

Повертає **`true`**, якщо параметр `var` не існує, якщо значення дорівнює нулю, або не задано, дивіться [Преобразование в булев тип](language.types.boolean.md#language.types.boolean.casting). В іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Просте порівняння **empty()** і [isset()](function.isset.md)**

```php
<?php
$var = 0;

// Принимает значение true, потому что $var пусто
if (empty($var)) {
    echo '$var или 0, или пусто, или вообще не определена';
}

// Принимает значение true, потому что $var определена
if (isset($var)) {
    echo '$var определена, даже если она пустая';
}
?>
```

**Приклад #2 **empty()** та рядкові індекси**

```php
<?php
$expected_array_got_string = 'somestring';
var_dump(empty($expected_array_got_string['some_key']));
var_dump(empty($expected_array_got_string[0]));
var_dump(empty($expected_array_got_string['0']));
var_dump(empty($expected_array_got_string[0.5]));
var_dump(empty($expected_array_got_string['0.5']));
var_dump(empty($expected_array_got_string['0 Mostel']));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(false)
bool(false)
bool(true)
bool(true)
```

### Примітки

> **Зауваження**: Оскільки це мовна конструкція, а не функція, вона не може викликатися за допомогою [змінних функцій](functions.variable-functions.md) або [іменованих аргументів](functions.arguments.md#functions.named-arguments)

> **Зауваження**
> 
> При використанні функції **empty()** на недоступних (неоголошених) властивостях об'єкта буде викликано вбудований метод об'єкту [isset()](language.oop5.overloading.md#object.isset)якщо він визначений.

### Дивіться також

-   [isset()](function.isset.md) - Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [isset()](language.oop5.overloading.md#object.isset)
-   [unset()](function.unset.md) - Видаляє змінну
-   [arraykeyexists()](function.array-key-exists.md) - Перевіряє, чи присутній у масиві зазначений ключ чи індекс
-   [count()](function.count.md) - Підраховує кількість елементів масиву або Countable об'єкті
-   [strlen()](function.strlen.md) - Повертає довжину рядка
-   [Таблица сравнения типов](types.comparisons.md)
