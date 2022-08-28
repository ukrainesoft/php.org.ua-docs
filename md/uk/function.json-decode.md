Декодує рядок JSON

-   [« Функции JSON](ref.json.html)
    
-   [json\_encode »](function.json-encode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции JSON](ref.json.html)
    
-   Декодує рядок JSON
    

# jsondecode

(PHP 5> = 5.2.0, PHP 7, PHP 8, PECL json> = 1.2.0)

jsondecode — Декодує рядок JSON

### Опис

```methodsynopsis
json_decode(    string $json,    ?bool $associative = null,    int $depth = 512,    int $flags = 0): mixed
```

Приймає закодований у JSON рядок і перетворює його на змінну PHP.

### Список параметрів

`json`

Рядок (string) `json` для декодування.

Функція працює тільки з рядками кодування UTF-8.

> **Зауваження**
> 
> PHP реалізує надмножина JSON, який описаний у початковому [» RFC 7159](http://www.faqs.org/rfcs/rfc7159)

`associative`

Якщо **`true`**, об'єкти JSON будуть повернуті як асоціативні масиви (array); якщо **`false`**, об'єкти JSON будуть повернуті як об'єкти (object). Якщо **`null`**, об'єкти JSON будуть повернуті як асоціативні масиви (array) або об'єкти (object) в залежності від того, чи встановлена **`JSON_OBJECT_AS_ARRAY`** в `flags`

`depth`

Максимальна глибина вкладеності структури, на яку проводитиметься декодування. Значення має бути більшим `0` і менше чи одно `2147483647`

`flags`

Бітова маска з констант **`JSON_BIGINT_AS_STRING`** **`JSON_INVALID_UTF8_IGNORE`** **`JSON_INVALID_UTF8_SUBSTITUTE`** **`JSON_OBJECT_AS_ARRAY`** **`JSON_THROW_ON_ERROR`**. Поведінка цих констант описано на сторінці [JSON-констант](json.constants.html)

### Значення, що повертаються

Повертає дані `json`, перетворені на відповідні типи PHP. Значення `true` `false` і `null` повертаються як **`true`** **`false`** і **`null`** відповідно . **`null`** також повертається, якщо `json` не може бути перетворений або закодовані дані містять вкладених рівнів більше, ніж зазначена межа вкладеності.

### Помилки

Починаючи з PHP 8.0.0, якщо значення параметра `depth` виходить за межі допустимого діапазону, функція викидає виняток [ValueError](class.valueerror.html); раніше видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано константу **`JSON_THROW_ON_ERROR`** для параметра `flags` |
|  | `associative` тепер nullable. |
|  | Додані константи **`JSON_INVALID_UTF8_IGNORE`** і **`JSON_INVALID_UTF8_SUBSTITUTE`** для параметра `flags` |
|  | Порожній ключ JSON ("") буде перетворено на порожню властивість об'єкта, а не на властивість зі значенням `_empty_` |

### Приклади

**Приклад #1 Приклади використання **jsondecode()****

```php
<?php
$json = '{"a":1,"b":2,"c":3,"d":4,"e":5}';

var_dump(json_decode($json));
var_dump(json_decode($json, true));

?>
```

Результат виконання цього прикладу:

```
object(stdClass)#1 (5) {
    ["a"] => int(1)
    ["b"] => int(2)
    ["c"] => int(3)
    ["d"] => int(4)
    ["e"] => int(5)
}

array(5) {
    ["a"] => int(1)
    ["b"] => int(2)
    ["c"] => int(3)
    ["d"] => int(4)
    ["e"] => int(5)
}
```

**Приклад #2 Доступ до властивостей об'єктів із неправильними іменами**

Доступ до елементів об'єкта, які містять символи, неприпустимі відповідно до угоди про імена PHP (тобто дефіс), може бути виконаний шляхом обрамлення імені елемента фігурними дужками та апострофами.

```php
<?php

$json = '{"foo-bar": 12345}';

$obj = json_decode($json);
print $obj->{'foo-bar'}; // 12345

?>
```

**Приклад #3 Поширена помилка під час використання **jsondecode()****

```php
<?php

// Следующие строки являются валидным кодом JavaScript, но не валидными JSON-данными

// Имя и значение должны помещаться в двойные кавычки
// Одинарные кавычки использовать нельзя
$bad_json = "{ 'bar': 'baz' }";
json_decode($bad_json); // null

// Имя должно обрамляться в двойные кавычки
$bad_json = '{ bar: "baz" }';
json_decode($bad_json); // null

// Не должно быть завершающей запятой (без последующего элемента)
$bad_json = '{ bar: "baz", }';
json_decode($bad_json); // null

?>
```

**Приклад #4 Помилки з глибиною вкладених об'єктів (`depth`**

```php
<?php
// Закодируем данные с глубиной вложенности 4 (array -> array -> array -> string).
$json = json_encode(
    array(
        1 => array(
            'English' => array(
                'One',
                'January'
            ),
            'French' => array(
                'Une',
                'Janvier'
            )
        )
    )
);

// Напечатаем ошибки для разных глубин.
var_dump(json_decode($json, true, 4));
echo 'Последняя ошибка: ', json_last_error_msg(), PHP_EOL, PHP_EOL;

var_dump(json_decode($json, true, 3));
echo 'Последняя ошибка: ', json_last_error_msg(), PHP_EOL, PHP_EOL;
?>
```

Результат виконання цього прикладу:

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
Последняя ошибка: No error

NULL
Последняя ошибка: Maximum stack depth exceeded
```

**Приклад #5 **jsondecode()** з великими цілими числами**

```php
<?php
$json = '{"number": 12345678901234567890}';

var_dump(json_decode($json));
var_dump(json_decode($json, false, 512, JSON_BIGINT_AS_STRING));

?>
```

Результат виконання цього прикладу:

```
object(stdClass)#1 (1) {
  ["number"]=>
  float(1.2345678901235E+19)
}
object(stdClass)#1 (1) {
  ["number"]=>
  string(20) "12345678901234567890"
}
```

### Примітки

> **Зауваження**
> 
> Специфікація JSON – це не JavaScript, а його підмножина.

> **Зауваження**
> 
> У разі виникнення помилки декодування можна використовувати [json\_last\_error()](function.json-last-error.html) визначення її причини.

### Дивіться також

-   [json\_encode()](function.json-encode.html) - Повертає JSON-подання даних
-   [json\_last\_error()](function.json-last-error.html) - Повертає останню помилку