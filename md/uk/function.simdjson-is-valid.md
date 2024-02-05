---
navigation:
  - function.simdjson-decode.md: « simdjson\_decode
  - function.simdjson-key-count.md: simdjson\_key\_count »
  - index.md: PHP Manual
  - ref.simdjson.md: Функції Simdjson
title: simdjson\_is\_valid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# simdjson\_is\_valid

(PECL simdjson >= 2.0.0)

simdjson\_is\_valid — Перевіряє, чи є рядок JSON коректним.

### Опис

```methodsynopsis
simdjson_is_valid(string $json = false, int $depth = 512): bool
```

Приймає рядок, закодований JSON і повертає true, якщо він коректний.

### Список параметрів

`json`

Строка (string) в формате`json` для перевірки.

Функція працює тільки з рядками кодування UTF-8.

Функція аналізує допустимі вхідні дані, які функція [json\_decode()](function.json-decode.md) може декодувати, за умови, що їхня довжина не перевищує 4 Гб.

`depth`

Максимальна глибина вкладеності структури, що декодується. Значення має бути більшим і менше чи одно `2147483647`. Команда, що викликає, повинна використовувати досить маленькі значення, оскільки велика глибина вимагають більше місця в буфері і збільшують глибину рекурсії, на відміну від поточної реалізації функції [json\_decode()](function.json-decode.md)

### Значення, що повертаються

Повертає **`true`**, якщо параметр `json` є коректним рядком JSON, інакше повертає **`false`**

### Помилки

Якщо параметр `json` більше 4 ГБ, то починаючи з версії PECL simdjson 2.1.0 викидається виняток [SimdJsonException](class.simdjsonexception.md); раніше викидався виняток [RuntimeException](class.runtimeexception.md)

Якщо параметр `depth` знаходиться поза допустимим діапазоном, то починаючи з версії PECL simdjson 3.0.0 викидається виняток [SimdJsonValueError](class.simdjsonvalueerror.md), тоді як раніше видавалася помилка рівня **`E_WARNING`**

### Приклади

**Пример #1 Пример использования[simdjson\_decode()](function.simdjson-decode.md)**

```php
<?php
$json = '{"a":1,"b":2,"c":3}';
$invalidJson = '{"a":1,"b":2,"c":';

var_dump(simdjson_is_valid($json));
var_dump(simdjson_is_valid($invalidJson));

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

**Пример #2 Ошибки`depth`**

```php
<?php
// Кодирование данных с максимальной глубиной 4
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

// Отображает ошибки для разных глубин.
var_dump(simdjson_is_valid($json, 4));
var_dump(simdjson_is_valid($json, 3));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
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
