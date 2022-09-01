---
navigation:
  - mongodb-driver-readpreference.bsonserialize.html: '« MongoDBDriverReadPreference::bsonSerialize'
  - mongodb-driver-readpreference.gethedge.html: 'MongoDBDriverReadPreference::getHedge »'
  - index.html: PHP Manual
  - class.mongodb-driver-readpreference.html: MongoDBDriverReadPreference
title: 'MongoDBDriverReadPreference::construct'
---
# MongoDBDriverReadPreference::construct

(mongodb >=1.0.0)

MongoDBDriverReadPreference::construct — Створити новий ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::__construct(string|int $mode, ?array $tagSets = null, ?array $options = null)
```

Створює новий [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html)що є незмінним об'єктом значення.

### Список параметрів

`mode`

**Режим переваги читання**

| Значение | Описание |
| --- | --- |
| **`MongoDB\Driver\ReadPreference::RP_PRIMARY`** ор `"primary"` |  |
| Усі операції зчитується з поточного первинного вузла реплік набору. Це перевага для читання за промовчанням для MongoDB. |  |

**`MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED`** ор `"primaryPreferred"`

У більшості ситуацій операції зчитуються з первинного вузла, але якщо він недоступний, операції зчитуються з вторинних вузлів.

**`MongoDB\Driver\ReadPreference::RP_SECONDARY`** або `"secondary"`

Усі операції зчитуються із вторинних вузлів набору реплік.

**`MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED`** або `"secondaryPreferred"`

Більшість ситуацій операції зчитуються з вторинних членів, але якщо вторинні члени недоступні, операції зчитуються з первинного вузла.

**`MongoDB\Driver\ReadPreference::RP_NEAREST`** ор `"nearest"`

Операції зчитуються з члена набору реплік із найменшою затримкою мережі, незалежно від типу члена.

`tagSets`

Набори тегів дозволяють настроювати операції читання для певних членів набору реплік. Цей параметр повинен бути масивом асоціативних масивів, кожен з яких містить нуль або кілька пар ключ-значення. При виборі сервера для операції читання драйвер намагається вибрати вузол, що має всі теги в наборі (тобто асоціативний масив пар ключ-значення). Якщо вибір не вдався, driver will attempt subsequent sets. Порожній набір тегів (`array()`) буде відповідати будь-якому вузлу і може використовуватись як резервний.

Теги не сумісні з режимом **`MongoDB\Driver\ReadPreference::RP_PRIMARY`**, і, зазвичай, застосовується лише за виборі вторинного члена набору для операції читання. Однак режим **`MongoDB\Driver\ReadPreference::RP_NEAREST`** у поєднанні з набором тегів вибирає відповідний член з найменшою затримкою мережі. Цей член може бути первинним чи вторинним.

`options`

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| hedge | object | array |
| Вказує, чи використовувати [» хеджовані читання](https://www.mongodb.com/docs/manual/core/sharded-cluster-query-router/#mongos-hedged-reads), що підтримуються MongoDB 4.4+ для закритих запитів. |  |  |

Хеджовані читання з сервера доступні для всіх неосновних переваг читання та включаються за умовчанням під час використання режиму `"nearest"`. Цей параметр дозволяє явно дозволити читання з хеджування на сервері для неосновних переваг читання, вказавши `['enabled' => true]`, або явно відключивши серверне читання з хеджуванням для переваг читання `"nearest"`, вказавши `['enabled' => false]`

| | maxStalenessSeconds | int |

Визначає максимальне відставання реплікації чи “staleness” для читання з вторинних вузлів. Коли оцінювана staleness вторинних вузлів перевищує це значення, драйвер припиняє використовувати її для операцій читання.

Якщо вказано, максимальний staleness має бути 32-бітовим числом без знака, більшим чи рівним **`MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS`**

За замовчуванням використовується **`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`**, що означає, що драйвер не враховуватиме відставання вторинних вузлів при виборі напрямку для операції читання.

Цей параметр несумісний із режимом **`MongoDB\Driver\ReadPreference::RP_PRIMARY`**. Вказівка ​​максимальної staleness також вимагає, щоб усі екземпляри MongoDB у розгортанні використовували MongoDB 3.4+. Виняток буде викинуто під час виконання, якщо екземпляри MongoDB у розгортанні мають старішу версію.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При некоректному `mode` викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Якщо `tagSets` надається як первинна перевага читання або має неправильний формат (тобто не масив з нуля або більше документів) викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Якщо опція `"maxStalenessSeconds"` надається для первинної переваги читання або знаходиться поза діапазоном, викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.8.0 | Доданий параметр `"hedge"` |
| PECL mongodb 1.3.0 |  |
| Аргумент `mode` тепер набуває рядкового значення, яке відповідає URI-опції `"readPreference"` для [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.html) |  |

| | PECL mongodb 1.2.0

Доданий третій аргумент `options`, який підтримує параметр `"maxStalenessSeconds"`

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadPreference::construct()****

```php
<?php

/* Предпочитать вторичный узел, но в случае отказа отступить к первичному. */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED));

/* Предпочитать узел в Нью-Йоркском центре обработки данных с минимальной задержкой. */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_NEAREST, [['dc' => 'ny']]));

/* Требуется дополнительный узел, чья задержка репликации находится в пределах двух минут от основного */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, ['maxStalenessSeconds' => 120]));

/* Явно включить хеджирование чтения на сервере */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, ['hedge' => ['enabled' => true]]));

?>
```

Результат виконання цього прикладу:

```
object(MongoDB\Driver\ReadPreference)#1 (1) {
  ["mode"]=>
  string(18) "secondaryPreferred"
}
object(MongoDB\Driver\ReadPreference)#1 (2) {
  ["mode"]=>
  string(7) "nearest"
  ["tags"]=>
  array(1) {
    [0]=>
    object(stdClass)#2 (1) {
      ["dc"]=>
      string(2) "ny"
    }
  }
}
object(MongoDB\Driver\ReadPreference)#1 (2) {
  ["mode"]=>
  string(9) "secondary"
  ["maxStalenessSeconds"]=>
  int(120)
}
object(MongoDB\Driver\ReadPreference)#1 (2) {
  ["mode"]=>
  string(9) "secondary"
  ["hedge"]=>
  object(stdClass)#1 (1) {
    ["enabled"]=>
    bool(true)
  }
}
```

### Дивіться також

-   [» Руководство по предпочтению чтения](https://www.mongodb.com/docs/manual/core/read-preference/)
