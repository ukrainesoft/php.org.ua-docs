- [« MongoDB\Driver\ReadPreference::getModeString](mongodb-driver-readpreference.getmodestring.md)
- [MongoDB\Driver\ReadPreference::serialize »](mongodb-driver-readpreference.serialize.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\ReadPreference](class.mongodb-driver-readpreference.md)
- Повертає параметр "tagSets" ReadPreference

# MongoDB\Driver\ReadPreference::getTagSets

(mongodb \>=1.0.0)

MongoDB\Driver\ReadPreference::getTagSets — Повертає параметр
"tagSets" ReadPreference

### Опис

final public **MongoDB\Driver\ReadPreference::getTagSets**(): array

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає параметр "tagSets" ReadPreference.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\ReadPreference::getTagSets()****

` <?php$mode =MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED;/* Як і null, так і порожній масив, позначають, що не будуть встановлені теги */$rp = new MongoDB\Driver\ReadPreference($mode, null);var_dump($rp->getTagSets());$rp = new MongoDB\Driver\ReadPreference($mode, []);var_dump($rp ->getTagSets());/* Вибрати вузол в Нью-Йорку, але повернутись до любому доступному резервному вузлу. */$rp = new MongoDB\Driver\ReadPreference($mode, [['dc' => 'ny']]);var_dump($rp->getTagSets());/* Вибрати вузол в Нью-Йорку, за яким|слід| */$rp = new MongoDB\Driver\ReadPreference($mode, [ ['dc' => 'ny'], ['dc' => 'sf', 'use' => 'reporting'],  [] ]);var_dump($rp->getTagSets());?> `

Результат виконання цього прикладу:

array(0) {
}
array(0) {
}
array(2) {
[0]=>
array(1) {
["dc"]=>
string(2) "ny"
}
[1]=>
array(0) {
}
}
array(3) {
[0]=>
array(1) {
["dc"]=>
string(2) "ny"
}
[1]=>
array(2) {
["dc"]=>
string(2) "sf"
["use"]=>
string(9) "reporting"
}
[2]=>
array(0) {
}
}

### Дивіться також

- [» Довідкова інформація за перевагою читання](https://www.mongodb.com/docs/manual/core/read-preference/)
