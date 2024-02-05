---
navigation:
  - ref.simdjson.md: « Функції Simdjson
  - function.simdjson-is-valid.md: simdjson\_is\_valid »
  - index.md: PHP Manual
  - ref.simdjson.md: Функції Simdjson
title: simdjson\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# simdjson\_decode

(PECL simdjson >= 2.0.0)

simdjson\_decode — Декодує рядок JSON

### Опис

```methodsynopsis
simdjson_decode(string $json, bool $associative = false, int $depth = 512): mixed
```

Приймає рядок у кодуванні JSON і перетворює його на значення PHP. При цьому буде використано швидшу реалізацію Simultaneous Instruction, Multiple Data, ніж у функції [json\_decode()](function.json-decode.md)якщо це підтримується архітектурою комп'ютера.

### Список параметрів

`json`

Декодований рядок (string) в `json`формате.

Функція працює тільки з рядками кодування UTF-8.

Функція аналізує допустимі вхідні дані, які функція [json\_decode()](function.json-decode.md) може декодувати, за умови, що їхня довжина не перевищує 4 Гб.

`associative`

При значении\*\*`true`\*\*, об'єкти JSON будуть повернуті як асоціативні масиви (array); при значенні **`false`**, об'єкти JSON будуть повернуті як об'єкти (object).

`depth`

Максимальна глибина вкладеності структури, що декодується. Значення має бути більшим і менше чи одно `2147483647`. Команда, що викликає, повинна використовувати досить маленькі значення, оскільки велика глибина вимагають більше місця в буфері і збільшують глибину рекурсії, на відміну від поточної реалізації функції [json\_decode()](function.json-decode.md)

### Значення, що повертаються

Повертає значення, закодоване у параметрі `json` у відповідному типі PHP. Значення `true` `false`и`null` повертаються як **`true`** \*\*`false`**и**`null`\*\*соответственно.

### Помилки

Якщо параметр `json` недійсний, то починаючи з версії PECL simdjson 2.1.0 викидається виняток [SimdJsonException](class.simdjsonexception.md), тоді як раніше викидався виняток [RuntimeException](class.runtimeexception.md)

Якщо параметр `depth` знаходиться поза допустимим діапазоном, то починаючи з версії PECL simdjson 3.0.0 викидається виняток [SimdJsonValueError](class.simdjsonvalueerror.md), тоді як раніше видавалася помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклади використання **simdjson\_decode()****

```php
<?php
$json = '{"a":1,"b":2,"c":3}';

var_dump(simdjson_decode($json));
var_dump(simdjson_decode($json, true));

?>
```

Результат виконання наведеного прикладу:

```
object(stdClass)#1 (3) {
  ["a"]=>
  int(1)
  ["b"]=>
  int(2)
  ["c"]=>
  int(3)
}
array(3) {
  ["a"]=>
  int(1)
  ["b"]=>
  int(2)
  ["c"]=>
  int(3)
}
```

**Приклад #2 Доступ до неприпустимих властивостей об'єкта**

Доступ до елементів об'єкта, що містять символи, не дозволені угодою PHP про іменування (наприклад, дефіс), може бути здійснений шляхом укладання імені елемента у фігурні дужки та апостроф.

```php
<?php

$json = '{"foo-bar": 12345}';

$obj = simdjson_decode($json);
print $obj->{'foo-bar'}; // 12345

?>
```

**Приклад #3 Поширені помилки під час використання **simdjson\_decode()****

```php
<?php

// следующие строки являются допустимыми JavaScript, но не являются допустимыми JSON

// имя и значение должны быть заключены в двойные кавычки
// одинарные кавычки недопустимы
$bad_json = "{ 'bar': 'baz' }";
simdjson_decode($bad_json); // Выбрасывается исключение SimdJsonException

// имя должно быть заключено в двойные кавычки
$bad_json = '{ bar: "baz" }';
simdjson_decode($bad_json); // Выбрасывается исключение SimdJsonException

// запятые в конце не допускаются
$bad_json = '{ bar: "baz", }';
simdjson_decode($bad_json); // Выбрасывается исключение SimdJsonException

?>
```

**Пример #4 Ошибки`depth`**

```php
<?php
// Кодирование некоторых данных с максимальной глубиной 4
// (array -> array -> array -> string)
$json = json_encode(
    [
        1 => [
            'English' => [
                'One',
                'January'
            ],
            'French' => [
                'Une',
                'Janvier'
            ]
        ]
    ]
);

// Отображение ошибок для разных глубин.
var_dump(simdjson_decode($json, true, 4));
try {
    var_dump(simdjson_decode($json, true, 3));
} catch (SimdJsonException $e) {
     echo "Попался: ", $e->getMessage(), "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  [1]=>
  array(2) {
    ["English"]=>
    array(2) {
      [0]=>
      string(3) "One"
      [1]=>
      string(7) "January"
    }
    ["French"]=>
    array(2) {
      [0]=>
      string(3) "Une"
      [1]=>
      string(7) "Janvier"
    }
  }
}
Попался: The JSON document was too deep (too many nested objects and arrays)
```

**Пример #5**simdjson\_decode()\*\* великих цілих чисел\*\*

```php
<?php
$json = '{"number": 12345678901234567890}';

var_dump(simdjson_decode($json));

?>
```

Результат виконання наведеного прикладу:

```
object(stdClass)#1 (1) {
  ["number"]=>
  float(1.2345678901235E+19)
}
```

### Примітки

> **Зауваження** :
> 
> Специфікація JSON - це не JavaScript, а підмножина JavaScript.

> **Зауваження** :
> 
> У разі виникнення помилки декодування викидається виняток [SimdJsonException](class.simdjsonexception.md), а**SimdJsonException::getCode()**и**SimdJsonException::getMessage()** можуть бути використані визначення точної природи помилки.

### Дивіться також

-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [json\_decode()](function.json-decode.md) \- Декодує рядок JSON
