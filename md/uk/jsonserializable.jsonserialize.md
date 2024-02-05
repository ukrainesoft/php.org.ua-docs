---
navigation:
  - class.jsonserializable.md: « JsonSerializable
  - ref.json.md: Функції JSON »
  - index.md: PHP Manual
  - class.jsonserializable.md: JsonSerializable
title: 'JsonSerializable::jsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# JsonSerializable::jsonSerialize

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

JsonSerializable::jsonSerialize — Задає дані, які мають бути серіалізовані в JSON

### Опис

```methodsynopsis
public JsonSerializable::jsonSerialize(): mixed
```

Серіалізує об'єкт значення, яке спочатку може бути серіалізоване функцією [json\_encode()](function.json-encode.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані [json\_encode()](function.json-encode.md), які є значенням будь-якого типу, крім [resource](language.types.resource.md)

### Приклади

**Пример #1 Пример использования**JsonSerializable::jsonSerialize()**, що повертає масив (array)**

```php
<?php

class ArrayValue implements JsonSerializable {
    private $array;
    public function __construct(array $array) {
        $this->array = $array;
    }

    public function jsonSerialize(): mixed {
        return $this->array;
    }
}

$array = [1, 2, 3];
echo json_encode(new ArrayValue($array), JSON_PRETTY_PRINT);
?>
```

Результат виконання наведеного прикладу:

```
[
    1,
    2,
    3
]
```

**Пример #2 Пример использования**JsonSerializable::jsonSerialize()**, що повертає асоціативний масив (array)**

```php
<?php

class ArrayValue implements JsonSerializable {
    private $array;
    public function __construct(array $array) {
        $this->array = $array;
    }

    public function jsonSerialize() {
        return $this->array;
    }
}

$array = ['foo' => 'bar', 'quux' => 'baz'];
echo json_encode(new ArrayValue($array), JSON_PRETTY_PRINT);
?>
```

Результат виконання наведеного прикладу:

```
{
    "foo": "bar",
    "quux": "baz"
}
```

**Пример #3 Пример использования**JsonSerializable::jsonSerialize()**, що повертає ціле значення (int)**

```php
<?php

class IntegerValue implements JsonSerializable {
    private $number;
    public function __construct($number) {
        $this->number = (int) $number;
    }

    public function jsonSerialize() {
        return $this->number;
    }
}

echo json_encode(new IntegerValue(1), JSON_PRETTY_PRINT);
?>
```

Результат виконання наведеного прикладу:

```
1
```

**Пример #4 Пример использования**JsonSerializable::jsonSerialize()**, що повертає рядок (string)**

```php
<?php

class StringValue implements JsonSerializable {
    private $string;
    public function __construct($string) {
        $this->string = (string) $string;
    }

    public function jsonSerialize() {
        return $this->string;
    }
}

echo json_encode(new StringValue('Hello!'), JSON_PRETTY_PRINT);
?>
```

Результат виконання наведеного прикладу:

```
"Hello!"
```
