---
navigation:
  - mongodb-driver-readpreference.getmodestring.md: '« MongoDB\\Driver\\ReadPreference::getModeString'
  - mongodb-driver-readpreference.serialize.md: 'MongoDB\\Driver\\ReadPreference::serialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::getTagSets'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::getTagSets

(mongodb >=1.0.0)

MongoDB\\Driver\\ReadPreference::getTagSets — Повертає параметр "tagSets" ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getTagSets(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає параметр "tagSets" ReadPreference.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\ReadPreference::getTagSets()\*\*\*\*

```php
<?php

$mode = MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED;

/* Как и null, так и пустой массив, обозначают, что не будут установлены теги для предпочтения. */
$rp = new MongoDB\Driver\ReadPreference($mode, null);
var_dump($rp->getTagSets());

$rp = new MongoDB\Driver\ReadPreference($mode, []);
var_dump($rp->getTagSets());

/* Выбрать узел в Нью-Йорке, но вернуться к любому доступному резервному узлу. */
$rp = new MongoDB\Driver\ReadPreference($mode, [['dc' => 'ny']]);
var_dump($rp->getTagSets());

/* Выбрать узел в Нью-Йорке, за которым следует узел в Сан-Франциско,
   который помечен для использования для отчётов, и, наконец, вернуться к любому доступному резервному узлу. */
$rp = new MongoDB\Driver\ReadPreference($mode, [
  ['dc' => 'ny'],
  ['dc' => 'sf', 'use' => 'reporting'],
  [],
]);
var_dump($rp->getTagSets());

?>
```

Результат виконання наведеного прикладу:

```
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
```

### Дивіться також

-   [» Довідкова інформація щодо переваги читання](https://www.mongodb.com/docs/manual/core/read-preference/)
