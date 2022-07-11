- [«filter_list](function.filter-list.md)
- [filter_var »](function.filter-var.md)

- [PHP Manual](index.md)
- [Функції фільтрації даних](ref.filter.md)
- приймає кілька змінних і, при необхідності, фільтрує їх

#filter_var_array

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

filter_var_array — Приймає кілька змінних і, за необхідності,
фільтрує їх

### Опис

**filter_var_array**(array `$array`, array\|int `$options` =
**`FILTER_DEFAULT`**, bool `$add_empty` = **`true`**):
array\|false\|null

Ця функція корисна для отримання множини змінних без багаторазового
виклик функції [filter_var()](function.filter-var.md).

### Список параметрів

`array`
Масив із рядковими ключами, що містить дані для фільтрації.

`options`
Масив, що визначає параметри. Допустимий ключ - рядок string,
містить ім'я змінної, а допустиме значення - [тип фільтра](filter.filters.md), або масив (array), за необхідності
визначальний фільтр, прапори та параметри. Якщо значення є масивом,
допустимими ключами є `filter`, який визначає [тип фільтра](filter.filters.md), `flags`, який визначає будь-які прапори,
застосовувані до фільтра, і `options`, який визначає будь-які параметри,
застосовувані до фільтру. Дивіться приклад нижче для кращого розуміння.

Цей параметр також може бути цілим числом, що містить
[визначену константу фільтра](filter.constants.md). Потім усі
значення у вхідному масиві фільтруються цим фільтром.

`add_empty`
Додає результат відсутні ключі зі значенням **`null`**.

### Значення, що повертаються

Масив, що містить значення запитаних змінних у разі успішного
виконання, або **`false`** у разі виникнення помилки. Значення
масиву буде **`false`**, якщо фільтрація завершилася невдачею, або
**`null`**, якщо змінна не визначена.

### Приклади

**Приклад #1 Приклад використання **filter_var_array()****

` <?php$data = array(    'product_id'    => 'libgd<script>',    'component'     => '10',    'versions'      => '2.0.33',    'testscalar'    => array('2 ', '23', '10', '12'),   'testarray'    => '2',);$args = array(    'product_id'             ¦ FILTER_VALIDATE_INT,                            'flags'     => FILTER_FORCE_ARRAY,                            'options'   => array('min_range' => 1, 'max_range' => 10)                           ),    'versions'     => FILTER_SANITIZE_ENCODED,    'doesnotexist' => FILTER_VALIDATE_INT,    'testscalar'   = > array(                            'filter' => FILTER_VALIDATE_INT,                            'flags'  => FILTER_REQUIRE_SCALAR,                           ),    'testarray'    => array(                            'filter' => FILTER_VALIDATE_INT,                            'flags'  => FILTER_FORCE_ARRAY,                           ));$myinputs = filter_var_array($data , $args);var_dump($myi nputs);echo "
";?> `

Результат виконання цього прикладу:

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

### Дивіться також

- [filter_input_array()](function.filter-input-array.md) - Отримує
кілька змінних ззовні PHP і, за необхідності, фільтрує їх
- [filter_var()](function.filter-var.md) - Фільтрує змінну з
допомогою певного фільтра
- [filter_input()](function.filter-input.md) - Приймає змінну
ззовні PHP і, при необхідності, фільтрує її
- [Типи фільтрів](filter.filters.md)
