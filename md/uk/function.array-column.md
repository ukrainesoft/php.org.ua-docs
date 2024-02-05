---
navigation:
  - function.array-chunk.md: « array\_chunk
  - function.array-combine.md: array\_combine »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_column
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_column

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

array\_column — Повертає масив із значень одного стовпця вхідного масиву

### Опис

```methodsynopsis
array_column(array $array, int|string|null $column_key, int|string|null $index_key = null): array
```

Функция**array\_column()** повертає значення одного стовпця масиву (`array`), обозначенного ключом`column_key`. Щоб проіндексувати значення масиву, що повертається, значеннями стовпця `index_key` вхідного масиву, задають необов'язковий параметр `index_key`

### Список параметрів

`array`

Багатомірний масив або масив об'єктів, з якого витягуватиметься стовпець значень. Якщо заданий масив об'єктів, то можна вибирати будь-які його загальнодоступні характеристики. Щоб отримати закриті або захищені властивості, у класі потрібно реалізувати два магічні методи. **\_\_get()**и**\_\_isset()**

`column_key`

Ключ шпальти, значення якого потрібно повернути. Дозволено передавати як цілий ключ стовпця, так і рядкову назву ключа асоціативного масиву або властивості об'єкта, значення якого потрібно отримати. У параметр також дозволено передавати значення **`null`** для повернення повних масивів або об'єктів (це буде корисно за умови одночасної передачі параметра `index_key`, щоб переіндексувати масив).

`index_key`

Стовпець, значення якого будуть ключами або індексами масива, що повертається. Дозволено вказувати як цілий ключ стовпця, так і рядкову назву ключа. Значення [наводиться](language.types.array.md#language.types.array.key-casts) як завжди для ключів масиву (проте, до PHP 8.0.0 об'єкти, що підтримують перетворення до рядка, були також дозволені).

### Значення, що повертаються

Повертає масив із значень одного стовпця чи властивості об'єкта вхідного масиву.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Об'єкти в стовпцях, позначені параметром `index_key`, більше не будуть перетворені на рядок і замість цього викидатимуть виняток [TypeError](class.typeerror.md) |

### Приклади

**Приклад #1 Отримаємо стовпець із іменами з набору записів**

```php
<?php

// Массив, представляющий набор записей, возвращённых из базы данных
$records = array(
    array(
        'id' => 2135,
        'first_name' => 'John',
        'last_name' => 'Doe',
    ),
    array(
        'id' => 3245,
        'first_name' => 'Sally',
        'last_name' => 'Smith',
    ),
    array(
        'id' => 5342,
        'first_name' => 'Jane',
        'last_name' => 'Jones',
    ),
    array(
        'id' => 5623,
        'first_name' => 'Peter',
        'last_name' => 'Doe',
    )
);

$first_names = array_column($records, 'first_name');
print_r($first_names);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => John
    [1] => Sally
    [2] => Jane
    [3] => Peter
)
```

**Приклад #2 Отримаємо стовпець прізвищ з набору записів, проіндексувавши їх значення стовпця «id»**

```php
<?php

// Используем массив $records из первого примера
$last_names = array_column($records, 'last_name', 'id');
print_r($last_names);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [2135] => Doe
    [3245] => Smith
    [5342] => Jones
    [5623] => Doe
)
```

**Приклад #3 Отримаємо стовпець імен користувачів із загальнодоступної властивості «username» об'єкта**

```php
<?php

class User
{
    public $username;

    public function __construct(string $username)
    {
        $this->username = $username;
    }
}

$users = [
    new User('user 1'),
    new User('user 2'),
    new User('user 3'),
];

print_r(array_column($users, 'username'));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => user 1
    [1] => user 2
    [2] => user 3
)
```

**Приклад #4 Отримаємо стовпець імен користувачів з приватної властивості об'єкта «name», визначивши магічний метод **\_\_get()****

```php
<?php

class Person
{
    private $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }

    public function __get($prop)
    {
        return $this->$prop;
    }

    public function __isset($prop) : bool
    {
        return isset($this->$prop);
    }
}

$people = [
    new Person('Fred'),
    new Person('Jane'),
    new Person('John'),
];

print_r(array_column($people, 'name'));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Fred
    [1] => Jane
    [2] => John
)
```

Якщо в об'єкті не буде методу **\_\_isset()**, то повернеться порожній масив.
