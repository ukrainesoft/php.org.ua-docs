---
navigation:
  - function.array-is-list.md: « arrayісlist
  - function.array-key-first.md: arraykeyfirst »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arraykeyexists
---
# arraykeyexists

(PHP 4> = 4.0.7, PHP 5, PHP 7, PHP 8)

arraykeyexists — Перевіряє, чи є у масиві зазначений ключ або індекс

### Опис

```methodsynopsis
array_key_exists(string|int $key, array $array): bool
```

Функція **arraykeyexists()** повертає \*\*`true`\*\*якщо в масиві присутній зазначений ключ `key`. Параметр `key` може бути будь-яким значенням, яке підходить для індексу масиву.

### Список параметрів

`key`

Перевірене значення.

`array`

Масив з ключами, що перевіряються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

> **Зауваження**
> 
> **arraykeyexists()** шукає ключі лише на першому рівні масиву. Внутрішні ключі в багатовимірних масивах не знайдено.

### Приклади

**Приклад #1 Приклад використання **arraykeyexists()****

```php
<?php
$search_array = array('first' => 1, 'second' => 4);
if (array_key_exists('first', $search_array)) {
    echo "Масив содержит элемент 'first'.";
}
?>
```

**Приклад #2 **arraykeyexists()** і [isset()](function.isset.md)**

[isset()](function.isset.md) не повертає **`true`** для ключів масиву, що вказують на **`null`**, а **arraykeyexists()** повертає.

```php
<?php
$search_array = array('first' => null, 'second' => 4);

// возвращает false
isset($search_array['first']);

// возвращает true
array_key_exists('first', $search_array);
?>
```

### Примітки

> **Зауваження**
> 
> З причин зворотної сумісності, **arraykeyexists()** повертає **`true`**, якщо `key` є властивістю об'єкта (object), переданим як параметр `array`. Поведінка застаріла у PHP 7.4.0 та видалена у PHP 8.0.0.
> 
> Щоб перевірити, чи містить об'єкт будь-яку властивість, використовуйте функцію [propertyexists()](function.property-exists.md)

### Дивіться також

-   [isset()](function.isset.md) - Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [arraykeys()](function.array-keys.md) - Повертає все або деяке підмножина ключів масиву
-   [інarray()](function.in-array.md) - Перевіряє, чи є у масиві значення
-   [propertyexists()](function.property-exists.md) - Перевіряє, чи містить об'єкт чи клас зазначений атрибут
