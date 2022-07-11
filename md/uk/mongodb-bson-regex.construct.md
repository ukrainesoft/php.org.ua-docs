- [«MongoDB\BSON\Regex](class.mongodb-bson-regex.md)
- [MongoDB\BSON\Regex::getFlags »](mongodb-bson-regex.getflags.md)

- [PHP Manual](index.md)
- [MongoDB\BSON\Regex](class.mongodb-bson-regex.md)
- Створює новий Regex

# MongoDB\BSON\Regex::\_\_construct

(mongodb \>=1.0.0)

MongoDB\BSON\Regex::\_\_construct — Створює новий Regex

### Опис

final public **MongoDB\BSON\Regex::\_\_construct**(string `$pattern`,
string `$flags` = "")

### Список параметрів

`pattern` (string)
Регулярний вираз шаблон.

> **Примітка**: Шаблон не повинен укладатися у символи-розділювачі.

`flags` (string)
[» Прапори регулярних виразів](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options).
Символи у цьому аргументі будуть відсортовані за абеткою.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).
- Видає
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md),
якщо `pattern` або `flags` містять нульові байти.

### Список змін

[TABLE]

### Приклади

**Приклад #1 Приклад використання
**MongoDB\BSON\Regex::\_\_construct()****

` <?php$regex = new MongoDB\BSON\Regex('^foo', 'i');var_dump($regex);?> `

Результат виконання цього прикладу:

object(MongoDB\BSON\Regex)#1 (2) {
["pattern"]=>
string(4) "^foo"
["flags"]=>
string(1) "i"
}

### Дивіться також

- [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
- [» Підтримувані прапори регулярних виразів](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)
