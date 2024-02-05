---
navigation:
  - class.mongodb-bson-regex.md: « MongoDB\\BSON\\Regex
  - mongodb-bson-regex.getflags.md: 'MongoDB\\BSON\\Regex::getFlags »'
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDB\\BSON\\Regex
title: 'MongoDB\\BSON\\Regex::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Regex::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\Regex::\_\_construct — Створює новий Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::__construct(string $pattern, string $flags = "")
```

### Список параметрів

`pattern`(string)

Шаблон регулярного виразу.

> **Зауваження**: Шаблон не повинен бути укладений у символи-розділювачі.

`flags`(string)

[» Прапори регулярних виразів](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options). Символи у цьому аргументі будуть відсортовані за абеткою.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `pattern`или`flags`містять нульові байти.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.2.0 |  |
| Аргумент`flags` є необов'язковим і за умовчанням дорівнює порожньому рядку. |  |

Символи в аргументі `flags` будуть відсортовані в алфавітному порядку під час побудови регулярного виразу. Раніше символи зберігалися у вказаному порядку.

Видається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `pattern`или`flags` містять нульові байти. Раніше значення були б обрізані у першому нульовому байті.

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Regex::\_\_construct()\*\*\*\*

```php
<?php

$regex = new MongoDB\BSON\Regex('^foo', 'i');
var_dump($regex);

?>
```

Результат виконання наведеного прикладу:

```
object(MongoDB\BSON\Regex)#1 (2) {
  ["pattern"]=>
  string(4) "^foo"
  ["flags"]=>
  string(1) "i"
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
-   [» Підтримувані прапори регулярних виразів](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)
