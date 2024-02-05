---
navigation:
  - function.filter-var-array.md: « filter\_var\_array
  - book.funchand.md: Управління функціями »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filter\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filter\_var

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

filter\_var — Фільтрує змінну за допомогою певного фільтра

### Опис

```methodsynopsis
filter_var(mixed $value, int $filter = FILTER_DEFAULT, array|int $options = 0): mixed
```

### Список параметрів

`value`

Значення змінної фільтрації. Зверніть увагу, що скалярні значення перед фільтрацією [перетворюються на рядки](language.types.string.md#language.types.string.casting)

`filter`

Ідентифікатор (ID) фільтра. На сторінці [Типи фільтрів](filter.filters.md) наведено список доступних фільтрів.

Если не указан, то принимает значение по умолчанию —\*\*`FILTER_DEFAULT`\*\*, який рівнозначний значенню константи [**`FILTER_UNSAFE_RAW`**](filter.filters.sanitize.md)То есть по умолчанию значение не фильтруется.

`options`

Асоціативний масив властивостей чи логічна диз'юнкція (операція АБО) прапорів. Якщо фільтр приймає настройки, прапори можуть бути вказані в елементі масиву "flags". Для фільтра "callback" має бути зазначений тип [callable](language.types.callable.md). . Фільтр "callback" повинен приймати один аргумент, значення фільтрації, і повертати значення після фільтрації.

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

// для фильтров, который принимает только флаги, вы также можете передать их как массив
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

**Пример #1 Пример использования**filter\_var()\*\*\*\*

```php
<?php
var_dump(filter_var('bob@example.com', FILTER_VALIDATE_EMAIL));
var_dump(filter_var('http://example.com', FILTER_VALIDATE_URL, FILTER_FLAG_PATH_REQUIRED));
?>
```

Результат виконання наведеного прикладу:

```
string(15) "bob@example.com"
bool(false)
```

**Приклад #2 Приклад фільтрації масиву**

```php
<?php

$emails = [
    "bob@example.com",
    "test@example.local",
    "invalidemail"
];

var_dump(filter_var($emails, FILTER_VALIDATE_EMAIL, FILTER_REQUIRE_ARRAY));
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  string(15) "bob@example.com"
  [1]=>
  string(18) "test@example.local"
  [2]=>
  bool(false)
}
```

### Дивіться також

-   [filter\_var\_array()](function.filter-var-array.md) \- приймає кілька змінних і, при необхідності, фільтрує їх
-   [filter\_input()](function.filter-input.md) \- приймає змінну ззовні PHP і, при необхідності, фільтрує її
-   [filter\_input\_array()](function.filter-input-array.md) \- Отримує кілька змінних ззовні PHP і, при необхідності, фільтрує їх
-   [Типи фільтрів](filter.filters.md)
