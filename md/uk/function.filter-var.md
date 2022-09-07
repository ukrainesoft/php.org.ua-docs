---
navigation:
  - function.filter-var-array.md: « filtervararray
  - book.funchand.md: Управление функциями »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filtervar
---
# filtervar

(PHP 5> = 5.2.0, PHP 7, PHP 8)

filtervar — Фільтрує змінну за допомогою певного фільтра

### Опис

```methodsynopsis
filter_var(mixed $value, int $filter = FILTER_DEFAULT, array|int $options = 0): mixed
```

### Список параметрів

`value`

Значення змінної фільтрації. Зверніть увагу, що скалярні значення перед фільтрацією [преобразуются к строкам](language.types.string.md#language.types.string.casting)

`filter`

Ідентифікатор (ID) фільтра. На сторінці [Типи фільтрів](filter.filters.md) наведено список доступних фільтрів.

Якщо не вказано, то використовується **`FILTER_DEFAULT`**, який рівнозначний [**`FILTER_UNSAFE_RAW`**](filter.filters.sanitize.md). Це означає, що за замовчуванням не застосовується фільтр.

`options`

Асоціативний масив властивостей чи логічна диз'юнкція (операція АБО) прапорів. Якщо фільтр приймає настройки, прапори можуть бути вказані в елементі масиву "flags". Для фільтра "callback" має бути вказаний тип [callable](language.types.callable.md). Фільтр "callback" повинен приймати один аргумент, значення фільтрації, і повертати значення після фільтрації.

```php
<?php
// используйте этот формат для фильтров с дополнительными параметрами
$options = array(
    'options' => array(
        'default' => 3, // значение, возвращаемое, если фильтрация завершилась неудачей
        // другие параметры
        'min_range' => 0
    ),
    'flags' => FILTER_FLAG_ALLOW_OCTAL,
);
$var = filter_var('0755', FILTER_VALIDATE_INT, $options);

// для фильтров, который принимает только флаги, вы можете передать их непосредственно
$var = filter_var('oops', FILTER_VALIDATE_BOOLEAN, FILTER_NULL_ON_FAILURE);

// для фильтров, который принимает только флаги, вы также можете передать их как Масив
$var = filter_var('oops', FILTER_VALIDATE_BOOLEAN,
                  array('flags' => FILTER_NULL_ON_FAILURE));

// callback-функция фильтра валидации
function foo($value)
{
    // Ожидаемый формат: Фамилия, Имена
    if (strpos($value, ", ") === false) return false;
    list($surname, $givennames) = explode(", ", $value, 2);
    $empty = (empty($surname) || empty($givennames));
    $notstrings = (!is_string($surname) || !is_string($givennames));
    if ($empty || $notstrings) {
        return false;
    } else {
        return $value;
    }
}
$var = filter_var('Doe, Jane Sue', FILTER_CALLBACK, array('options' => 'foo'));
?>
```

### Значення, що повертаються

Повертає відфільтровані дані або \*\*`false`\*\*якщо фільтрація завершилася невдачею.

### Приклади

**Приклад #1 Приклад використання **filtervar()****

```php
<?php
var_dump(filter_var('bob@example.com', FILTER_VALIDATE_EMAIL));
var_dump(filter_var('http://example.com', FILTER_VALIDATE_URL, FILTER_FLAG_PATH_REQUIRED));
?>
```

Результат виконання цього прикладу:

```
string(15) "bob@example.com"
bool(false)
```

### Дивіться також

-   [filtervararray()](function.filter-var-array.md) - приймає кілька змінних і, при необхідності, фільтрує їх
-   [filterinput()](function.filter-input.md) - приймає змінну ззовні PHP і, при необхідності, фільтрує її
-   [filterinputarray()](function.filter-input-array.md) - Отримує кілька змінних ззовні PHP і, при необхідності, фільтрує їх
-   [Типи фільтрів](filter.filters.md)
