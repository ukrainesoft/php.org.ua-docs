- [«filter_var_array](function.filter-var-array.md)
- [Керування функціями »](book.funchand.md)

- [PHP Manual](index.md)
- [Функції фільтрації даних](ref.filter.md)
- Фільтрує змінну за допомогою певного фільтра

#filter_var

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

filter_var — Фільтрує змінну за допомогою певного фільтра

### Опис

**filter_var**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`, int `$filter` = **`FILTER_DEFAULT`**, array\|int `$options` =
0):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

### Список параметрів

`value`
Значення змінної фільтрації. Зверніть увагу, що скалярні
значення перед фільтрацією [перетворюються до строк](language.types.string.md#language.types.string.casting).

`filter`
Ідентифікатор (ID) фільтра. На сторінці [Типи фільтрів](filter.filters.md) наведено список доступних фільтрів.

Якщо не вказано, то використовується **`FILTER_DEFAULT`**, який
рівнозначний [**`FILTER_UNSAFE_RAW`**](filter.filters.sanitize.md). Це
означає, що за умовчанням не застосовується фільтр.

`options`
Асоціативний масив властивостей або логічна диз'юнкція (операція
АБО) прапорів. Якщо фільтр приймає параметри, прапори можуть бути вказані в
елемент масиву "flags". Для фільтра "callback" має бути вказаний тип
[callable](language.types.callable.md). Фільтр "callback" повинен
приймати один аргумент, значення для фільтрації, та повертати значення
після фільтрації.

` <?php// используйте этот формат для фильтров с дополнительными параметрами$options = array(    'options' => array(        'default' => 3, // значение, возвращаемое, если фильтрация завершилась неудачей        // другие параметры        'min_range' => 0    ),    'flags' => FILTER_FLAG_ALLOW_OCTAL,);$var = filter_var('0755', FILTER_VALIDATE_INT, $options);// для фильтров, который принимает только флаги, вы можете передать их непосредственно$var = filter_var(' oops', FILTER_VALIDATE_BOOLEAN, FILTER_NULL_ON_FAILURE);// для фильтров, который принимает только флаги, вы также можете передать их как массив$var = filter_var('oops', FILTER_VALIDATE_BOOLEAN,                  array('flags' => FILTER_NULL_ON_FAILURE));// callback -функція фільтру валідаціїfunction foo($value){    // Очікуваний формат: Прізвище, Імена    if (strpos($value, ", ") === false) | list($surname, $givennames) =explode(", ", $value, 2); $empty==(empty($surname) || empty($givennames)); $notstrings = (!is_string($surname) || !is_string($givennames)); if ($empty |||$$notstrings) {       return false; } else {        return $value; }}$var = filter_var('Doe, Jane Sue', FILTER_CALLBACK, array('options' => 'foo'));?> `

### Значення, що повертаються

Повертає відфільтровані дані або **`false`**, якщо фільтрація
завершилася невдачею.

### Приклади

**Приклад #1 Приклад використання **filter_var()****

` <?phpvar_dump(filter_var('bob@example.com', FILTER_VALIDATE_EMAIL));var_dump(filter_var('http://example.com', FILTER_VALIDATE_URL, FILTER_FLAG_PATH_REQUIRED));?> `

Результат виконання цього прикладу:

string(15) "bob@example.com"
bool(false)

### Дивіться також

- [filter_var_array()](function.filter-var-array.md) - Приймає
кілька змінних і, при необхідності, фільтрує їх
- [filter_input()](function.filter-input.md) - Приймає змінну
ззовні PHP і, при необхідності, фільтрує її
- [filter_input_array()](function.filter-input-array.md) - Отримує
кілька змінних ззовні PHP і, за необхідності, фільтрує їх
- [Типи фільтрів](filter.filters.md)
