---
navigation:
  - function.simdjson-key-count.md: « simdjson\_key\_count
  - function.simdjson-key-value.md: simdjson\_key\_value »
  - index.md: PHP Manual
  - ref.simdjson.md: Функції Simdjson
title: simdjson\_key\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# simdjson\_key\_exists

(PECL simdjson >= 2.0.0)

simdjson\_key\_exists — Перевіряє, чи містить JSON значення, на яке посилається покажчик JSON

### Опис

```methodsynopsis
simdjson_key_exists(string $json, string $key, int $depth = ?): bool
```

Підраховує кількість елементів об'єкта/масиву, знайдених за запитаним покажчиком JSON.

### Список параметрів

`json`

Запрошуваний рядок (string) у форматі `json`

`key`

Рядок (string) покажчик JSON.

`depth`

Максимальна глибина вкладеності структури, що декодується. Значення має бути більшим і менше чи одно `2147483647`. Команда, що викликає, повинна використовувати досить маленькі значення, оскільки велика глибина вимагають більше місця в буфері і збільшують глибину рекурсії, на відміну від поточної реалізації функції [json\_decode()](function.json-decode.md)

`throw_if_uncountable`

При значении\*\*`true`\*\* замість значення 0, що повертається, буде викинуто виняток [SimdJsonException](class.simdjsonexception.md)якщо значення, на яке вказує покажчик JSON, не є ні об'єктом, ні масивом.

### Значення, що повертаються

Повертає **`true`**, якщо вказівник JSON є дійсним і посилається на значення, знайдене в коректному рядку JSON. Повертає \*\*`false`\*\*якщо JSON дійсний, але не містить покажчика JSON.
