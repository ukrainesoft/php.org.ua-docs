---
navigation:
  - class.jsonserializable.html: « JsonSerializable
  - ref.json.html: Функции JSON »
  - index.html: PHP Manual
  - class.jsonserializable.html: JsonSerializable
title: 'JsonSerializable::jsonSerialize'
---
# JsonSerializable::jsonSerialize

(PHP 5> = 5.4.0, PHP 7, PHP 8)

JsonSerializable::jsonSerialize — Задає дані, які мають бути серіалізовані в JSON

### Опис

```methodsynopsis
public JsonSerializable::jsonSerialize(): mixed
```

Серіалізує об'єкт значення, яке спочатку може бути серіалізоване функцією [jsonencode()](function.json-encode.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані [jsonencode()](function.json-encode.html), які є значенням будь-якого типу, крім [resource](language.types.resource.html)

### Приклади

**Приклад #1 Приклад використання **JsonSerializable::jsonSerialize()**, що повертає масив (array)**

```php
<?php
class ArrayValue implements JsonSerializable {
    public function __construct(array $array) {
        $this->array = $array;
    }

    public function jsonSerialize() {
        return $this->array;
    }
}

$array = [1, 2, 3];
echo json_encode(new ArrayValue($array), JSON_PRETTY_PRINT);
?>
```

Результат виконання цього прикладу:

```
[
    1,
    2,
    3
]
```

**Приклад #2 Приклад використання **JsonSerializable::jsonSerialize()**, що повертає асоціативний масив (array)**

```php
<?php
class ArrayValue implements JsonSerializable {
    public function __construct(array $array) {
        $this->array = $array;
    }

    public function jsonSerialize() {
        return $this->array;
    }
}

$array = ['foo' => 'bar', 'quux' => 'baz'];
echo json_encode(new ArrayValue($array), JSON_PRETTY_PRINT);
?>
```

Результат виконання цього прикладу:

```
{
    "foo": "bar",
    "quux": "baz"
}
```

**Приклад #3 Приклад використання **JsonSerializable::jsonSerialize()**, що повертає ціле значення (int)**

```php
<?php
class IntegerValue implements JsonSerializable {
    public function __construct($number) {
        $this->number = (integer) $number;
    }

    public function jsonSerialize() {
        return $this->number;
    }
}

echo json_encode(new IntegerValue(1), JSON_PRETTY_PRINT);
?>
```

Результат виконання цього прикладу:

```
1
```

**Приклад #4 Приклад використання **JsonSerializable::jsonSerialize()**, що повертає рядок (string)**

```php
<?php
class StringValue implements JsonSerializable {
    public function __construct($string) {
        $this->string = (string) $string;
    }

    public function jsonSerialize() {
        return $this->string;
    }
}

echo json_encode(new StringValue('Hello!'), JSON_PRETTY_PRINT);
?>
```

Результат виконання цього прикладу:

```
"Hello!"
```
