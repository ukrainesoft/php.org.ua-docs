---
navigation:
  - function.filter-id.md: « filter\_id
  - function.filter-input.md: filter\_input »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filter\_input\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filter\_input\_array

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

filter\_input\_array - Отримує кілька змінних ззовні PHP і, при необхідності, фільтрує їх

### Опис

```methodsynopsis
filter_input_array(int $type, array|int $options = FILTER_DEFAULT, bool $add_empty = true): array|false|null
```

Ця функція корисна для отримання множини змінних без багаторазового виклику функції [filter\_input()](function.filter-input.md)

### Список параметрів

`type`

Одна из констант\*\*`INPUT_GET`\*\* **`INPUT_POST`** **`INPUT_COOKIE`** **`INPUT_SERVER`** або **`INPUT_ENV`**

`options`

Масив, визначальний аргументи. Допустимий ключ - рядок (string), що містить ім'я змінної, а допустиме значення - або тип [фільтра](filter.filters.md), або масив (array), при необхідності визначальний фільтр, прапори та параметри. Якщо значення є масивом, допустимими ключами є `filter`, Який визначає ([тип фільтра](filter.filters.md) `flags`, який визначає будь-які прапори, що застосовуються до фільтра та `options`який визначає будь-які параметри, що застосовуються до фільтра. Дивіться нижче приклад для кращого розуміння.

Цей параметр також може бути цілим числом, що містить [зумовлену фільтрову константу](filter.constants.md). Потім усі значення у вхідному масиві фільтруються цим фільтром.

`add_empty`

Добавляет в результат отсутствующие ключи со значением\*\*`null`\*\*

### Значення, що повертаються

Масив, що містить значення змінених у разі успішного виконання. Якщо вхідний масив визначається параметром `type`, не заповнений, то функція поверне **`null`**, якщо прапор **`FILTER_NULL_ON_FAILURE`**не задан,**`false`** в іншому випадку. Для інших невдалих виконань повертається **`false`**

Значення масиву буде **`false`**, якщо фільтрація завершилася невдачею, або **`null`**, если переменная не определена. Либо, если установлен флаг\*\*`FILTER_NULL_ON_FAILURE`\*\*, повертається **`false`**, якщо змінна не визначена та **`null`**якщо фільтрація завершилася невдачею. Якщо параметр `add_empty`равен**`false`**, елемент масиву не буде додано для віддалених змінних.

### Приклади

**Приклад #1 Приклад використання** filter\_input\_array()\*\*\*\*

```php
<?php

/* данные, полученные методом POST
$_POST = array(
    'product_id' => 'libgd<script>',
    'component'  => array('10'),
    'version'    => '2.0.33',
    'testarray'  => array('2', '23', '10', '12'),
    'testscalar' => '2',
);
*/

$args = array(
    'product_id'   => FILTER_SANITIZE_ENCODED,
    'component'    => array('filter'    => FILTER_VALIDATE_INT,
                            'flags'     => FILTER_REQUIRE_ARRAY,
                            'options'   => array('min_range' => 1, 'max_range' => 10)
                           ),
    'version'      => FILTER_SANITIZE_ENCODED,
    'doesnotexist' => FILTER_VALIDATE_INT,
    'testscalar'   => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_REQUIRE_SCALAR,
                           ),
    'testarray'    => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_REQUIRE_ARRAY,
                           )

);

$myinputs = filter_input_array(INPUT_POST, $args);

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
  ["version"]=>
    string(6) "2.0.33"
  ["doesnotexist"]=>
  NULL
  ["testscalar"]=>
  int(2)
  ["testarray"]=>
  array(4) {
    [0]=>
    int(2)
    [1]=>
    int(23)
    [2]=>
    int(10)
    [3]=>
    int(12)
  }
}
```

### Примітки

> **Зауваження** :
> 
> У масиві **`INPUT_SERVER`** немає ключа `REQUEST_TIME`, тому що він буде пізніше в [$\_SERVER](reserved.variables.server.md)

### Дивіться також

-   [filter\_input()](function.filter-input.md) \- приймає змінну ззовні PHP і, при необхідності, фільтрує її
-   [filter\_var\_array()](function.filter-var-array.md) \- приймає кілька змінних і, при необхідності, фільтрує їх
-   [Типи фільтрів](filter.filters.md)
