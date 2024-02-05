---
navigation:
  - function.filter-list.md: « filter\_list
  - function.filter-var.md: filter\_var »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filter\_var\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filter\_var\_array

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

filter\_var\_array - Приймає кілька змінних і, при необхідності, фільтрує їх

### Опис

```methodsynopsis
filter_var_array(array $array, array|int $options = FILTER_DEFAULT, bool $add_empty = true): array|false|null
```

Ця функція корисна для отримання множини змінних без багаторазового виклику функції [filter\_var()](function.filter-var.md)

### Список параметрів

`array`

Масив із рядковими ключами, що містить дані для фільтрації.

`options`

Масив, що визначає параметри. Допустимий ключ - рядок string, що містить ім'я змінної, а допустиме значення - [тип фільтра](filter.filters.md), або масив (array), при необхідності визначальний фільтр, прапори та параметри. Якщо значення є масивом, допустимими ключами є `filter`, який визначає [тип фільтра](filter.filters.md) `flags`, який визначає будь-які прапори, що застосовуються до фільтра, та `options`який визначає будь-які параметри, що застосовуються до фільтра. Дивіться нижче приклад для кращого розуміння.

Цей параметр також може бути цілим числом, що містить [зумовлену константу фільтра](filter.constants.md). Потім усі значення у вхідному масиві фільтруються цим фільтром.

`add_empty`

Добавляет в результат отсутствующие ключи со значением\*\*`null`\*\*

### Значення, що повертаються

Масив, що містить значення запитаних змінних у разі успішного виконання, або **`false`** у разі виникнення помилки. Значення масиву буде **`false`**, якщо фільтрація завершилася невдачею, або \*\*`null`\*\*якщо змінна не визначена.

### Приклади

**Пример #1 Пример использования**filter\_var\_array()\*\*\*\*

```php
<?php

$data = array(
    'product_id'    => 'libgd<script>',
    'component'     => '10',
    'versions'      => '2.0.33',
    'testscalar'    => array('2', '23', '10', '12'),
    'testarray'     => '2',
);

$args = array(
    'product_id'   => FILTER_SANITIZE_ENCODED,
    'component'    => array('filter'    => FILTER_VALIDATE_INT,
                            'flags'     => FILTER_FORCE_ARRAY,
                            'options'   => array('min_range' => 1, 'max_range' => 10)
                           ),
    'versions'     => FILTER_SANITIZE_ENCODED,
    'doesnotexist' => FILTER_VALIDATE_INT,
    'testscalar'   => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_REQUIRE_SCALAR,
                           ),
    'testarray'    => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_FORCE_ARRAY,
                           )

);

$myinputs = filter_var_array($data, $args);

var_dump($myinputs);
echo "\n";
?>
```

Результат виконання наведеного прикладу:

```
array(6) {
  ["product_id"]=>
    string(17) "libgd%3Cscript%3E"
  ["component"]=>
  array(1) {
    [0]=>
    int(10)
  }
  ["versions"]=>
    string(6) "2.0.33"
  ["doesnotexist"]=>
  NULL
  ["testscalar"]=>
  bool(false)
  ["testarray"]=>
  array(1) {
    [0]=>
    int(2)
  }
}
```

### Дивіться також

-   [filter\_input\_array()](function.filter-input-array.md) \- Отримує кілька змінних ззовні PHP і, при необхідності, фільтрує їх
-   [filter\_var()](function.filter-var.md) \- Фільтрує змінну за допомогою певного фільтра
-   [filter\_input()](function.filter-input.md) \- приймає змінну ззовні PHP і, при необхідності, фільтрує її
-   [Типи фільтрів](filter.filters.md)
