Створює новий Regex

-   [« MongoDBBSONRegex](class.mongodb-bson-regex.html)
    
-   [MongoDBBSONRegex::getFlags »](mongodb-bson-regex.getflags.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONRegex](class.mongodb-bson-regex.html)
    
-   Створює новий Regex
    

# MongoDBBSONRegex::construct

(mongodb >=1.0.0)

MongoDBBSONRegex::construct — Створює новий Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::__construct(string $pattern, string $flags = "")
```

### Список параметрів

`pattern` (string)

Шаблон регулярного виразу.

> **Зауваження**: Шаблон не повинен бути укладений у символи-розділювачі.

`flags` (string)

[» Флаги регулярных выражений](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options). Символи у цьому аргументі будуть відсортовані за абеткою.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html), якщо `pattern` або `flags` містять нульові байти.

### список змін

| Версия                                                                       | Описание |
|------------------------------------------------------------------------------|----------|
| PECL mongodb 1.2.0                                                           |          |
| Аргумент `flags` є необов'язковим і за умовчанням дорівнює порожньому рядку. |          |

Символи в аргументі `flags` будуть відсортовані в алфавітному порядку під час побудови регулярного виразу. Раніше символи зберігалися у вказаному порядку.

Видається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html), якщо `pattern` або `flags` містять нульові байти. Раніше значення були б обрізані у першому нульовому байті.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONRegex::construct()****

```php
<?php

$regex = new MongoDB\BSON\Regex('^foo', 'i');
var_dump($regex);

?>
```

Результат виконання цього прикладу:

```
object(MongoDB\BSON\Regex)#1 (2) {
  ["pattern"]=>
  string(4) "^foo"
  ["flags"]=>
  string(1) "i"
}
```

### Дивіться також

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
-   [» Підтримувані прапори регулярних виразів](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)