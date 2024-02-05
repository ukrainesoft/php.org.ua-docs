---
navigation:
  - function.simdjson-key-exists.md: « simdjson\_key\_exists
  - class.simdjsonexception.md: SimdJsonException »
  - index.md: PHP Manual
  - ref.simdjson.md: Функції Simdjson
title: simdjson\_key\_value
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# simdjson\_key\_value

(PECL simdjson >= 2.0.0)

simdjson\_key\_value — Декодує значення рядка JSON, розташованого за запитаним покажчиком JSON

### Опис

```methodsynopsis
simdjson_key_value(    string $json,    string $key,    bool $associative = false,    int $depth = 512): mixed
```

Декодує та повертає значення, знайдене у запитаному покажчику JSON.

### Список параметрів

`json`

Запрошуваний та декодований рядок (string) у форматі `json`

Функція працює тільки з рядками кодування UTF-8.

Функція аналізує допустимі вхідні дані, які функція [json\_decode()](function.json-decode.md) може декодувати, за умови, що їхня довжина не перевищує 4 Гб.

`key`

Рядок (string) покажчик JSON.

`associative`

При значении\*\*`true`\*\*, об'єкти JSON будуть повернуті як асоціативні масиви (array); при значенні **`false`**, об'єкти JSON будуть повернуті як об'єкти (object).

`depth`

Максимальна глибина вкладеності структури, що декодується. Значення має бути більшим і менше чи одно `2147483647`. Команда, що викликає, повинна використовувати досить маленькі значення, оскільки велика глибина вимагають більше місця в буфері і збільшують глибину рекурсії, на відміну від поточної реалізації функції [json\_decode()](function.json-decode.md)

### Значення, що повертаються

Повертає частину значення, закодовану у параметрі `json` на яку посилається ключ `key` у відповідному PHP-типі. Значення `true` `false`и`null` повертаються як **`true`** \*\*`false`** і **`null`\*\*соответственно.

### Помилки

Якщо параметр `json`или`key` неприпустимі або параметр `key` не вдалося знайти у параметрі `json`, то починаючи з версії PECL simdjson 2.1.0 викидається виняток [SimdJsonException](class.simdjsonexception.md); раніше викидався виняток [RuntimeException](class.runtimeexception.md)

Якщо параметр `depth` знаходиться поза допустимим діапазоном, то починаючи з версії PECL simdjson 3.0.0 викидається виняток [SimdJsonValueError](class.simdjsonvalueerror.md), тоді як раніше видавалася помилка рівня **`E_WARNING`**

### Дивіться також

-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [simdjson\_decode()](function.simdjson-decode.md) \- Декодує рядок JSON
