---
navigation:
  - function.doubleval.md: « doubleval
  - function.floatval.md: floatval »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: empty
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# empty

(PHP 4, PHP 5, PHP 7, PHP 8)

empty — Перевіряє, чи порожня змінна

### Опис

```methodsynopsis
empty(mixed $var): bool
```

Перевіряє, чи вважається змінна пустою. Змінна вважається порожньою, якщо вона не існує або її значення дорівнює **`false`**. Мовна конструкція **empty()** не генерує попередження, якщо змінна немає.

### Список параметрів

`var`

Перевірена змінна.

Якщо змінна немає, попередження не генерується. Тобто конструкція **empty()** - це короткий еквівалент конструкції **!isset($var) || $var == false**

### Значення, що повертаються

Повертає **`true`**, якщо передана у параметр `var` змінна не існує, містить порожнє значення або дорівнює нулю, тобто хибно, докладніше про приведення значень до логічних типів, розказано в параграфі [перетворення на логічний тип](language.types.boolean.md#language.types.boolean.casting). В інших випадках повертає **`false`**

### Приклади

\*\*Приклад #1 Просте порівняння мовних конструкцій \*\*empty()**и[isset()](function.isset.md)**

```php
<?php
$var = 0;

// Принимает значение true, потому что переменная $var содержит пустое значение
if (empty($var)) {
    echo '$var или 0, или пусто, или вообще не определена';
}

// Принимает значение true, потому что переменная $var определена
if (isset($var)) {
    echo '$var определена, даже если она пустая';
}
?>
```

**Пример #2 Конструкция**empty()\*\* та рядкові індекси\*\*

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

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(false)
bool(false)
bool(true)
bool(true)
```

### Примітки

> **Зауваження**: Оскільки це мовна конструкція, а не функція, її не можна викликати як [змінну функцію](functions.variable-functions.md) або передавати як [іменований аргумент](functions.arguments.md#functions.named-arguments)

> **Зауваження** :
> 
> При виклику мовної конструкції **empty()** на недоступних (неоголошених, захищених або закритих) властивостях об'єкта викликається метод перевантаження. [\_\_isset()](language.oop5.overloading.md#object.isset)якщо він визначений.

### Дивіться також

-   [isset()](function.isset.md) \- Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [\_\_isset()](language.oop5.overloading.md#object.isset)
-   [unset()](function.unset.md) \- Видаляє змінну
-   [array\_key\_exists()](function.array-key-exists.md) \- Перевіряє, чи існує в масиві заданий ключ чи індекс
-   [count()](function.count.md) \- Підраховує кількість елементів масиву або Countable об'єкті
-   [strlen()](function.strlen.md) \- Повертає довжину рядка
-   [Таблиця порівняння типів](types.comparisons.md)
