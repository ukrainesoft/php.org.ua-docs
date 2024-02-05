---
navigation:
  - mongodb-driver-readpreference.bsonserialize.md: '« MongoDB\\Driver\\ReadPreference::bsonSerialize'
  - mongodb-driver-readpreference.gethedge.md: 'MongoDB\\Driver\\ReadPreference::getHedge »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::\_\_construct

(mongodb >=1.0.0)

MongoDB\\Driver\\ReadPreference::\_\_construct — Створити новий ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::__construct(string|int $mode, ?array $tagSets = null, ?array $options = null)
```

Створює новий [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)що є незмінним об'єктом значення.

### Список параметрів

`mode`

**Режим переваги читання**

| Значение | Опис |
| --- | --- |
| \*\*`MongoDB\Driver\ReadPreference::RP_PRIMARY`\*\*or`"primary"` |  |
| Усі операції зчитується з поточного первинного вузла реплік набору. Це перевага для читання за промовчанням для MongoDB. |  |

\*\*`MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED`\*\*or`"primaryPreferred"`

У більшості ситуацій операції зчитуються з первинного вузла, але якщо він недоступний, операції зчитуються з вторинних вузлів.

\*\*`MongoDB\Driver\ReadPreference::RP_SECONDARY`\*\*или`"secondary"`

Усі операції зчитуються із вторинних вузлів набору реплік.

\*\*`MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED`\*\*или`"secondaryPreferred"`

У більшості ситуацій операції зчитуються з вторинних членів, але якщо вторинні члени недоступні, операції зчитуються з первинного вузла.

\*\*`MongoDB\Driver\ReadPreference::RP_NEAREST`\*\*or`"nearest"`

Операції зчитуються з члена набору реплік із найменшою затримкою мережі, незалежно від типу члена.

`tagSets`

Набори тегів дозволяють настроювати операції читання для певних членів набору реплік. Цей параметр має бути масивом асоціативних масивів, кожен з яких містить нуль або кілька пар ключ-значення. При виборі сервера для операції читання драйвер намагається вибрати вузол, що має всі теги в наборі (тобто асоціативний масив пар ключ-значення). Якщо вибір не вдався, driver will attempt subsequent sets. Порожній набір тегів (`array()`) буде відповідати будь-якому вузлу і може використовуватись як резервний.

Теги не сумісні з режимом **`MongoDB\Driver\ReadPreference::RP_PRIMARY`**, і, зазвичай, застосовується лише за виборі вторинного члена набору для операції читання. Однак режим **`MongoDB\Driver\ReadPreference::RP_NEAREST`** у поєднанні з набором тегів вибирає відповідний член з найменшою затримкою мережі. Цей член може бути первинним чи вторинним.

`options`

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| hedge | object | array |
| Вказує, чи використовувати [» хеджовані читання](https://www.mongodb.com/docs/manual/core/sharded-cluster-query-router/#mongos-hedged-reads), що підтримуються MongoDB 4.4+ для закритих запитів. |  |  |

Хеджовані читання з сервера доступні для всіх неосновних переваг читання та включаються за умовчанням під час використання режиму `"nearest"`. Цей параметр дозволяє явно дозволити читання з хеджування на сервері для неосновних переваг читання, вказавши `['enabled' => true]`, або явно відключивши серверне читання з хеджуванням для переваг читання `"nearest"`, указав`['enabled' => false]`

| | maxStalenessSeconds | int |

Визначає максимальне відставання реплікації чи “staleness” для читання з вторинних вузлів. Коли оцінювана staleness вторинних вузлів перевищує це значення, драйвер припиняє використовувати її для операцій читання.

Якщо вказано, максимальний staleness має бути 32-бітовим числом без знака, більшим чи рівним **`MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS`**

По умолчанию используется\*\*`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`\*\*, що означає, що драйвер не враховуватиме відставання вторинних вузлів при виборі напрямку для операції читання.

Цей параметр несумісний із режимом **`MongoDB\Driver\ReadPreference::RP_PRIMARY`**. Вказівка ​​максимальної staleness також вимагає, щоб усі екземпляри MongoDB у розгортанні використовували MongoDB 3.4+. Виняток буде викинуто під час виконання, якщо екземпляри MongoDB у розгортанні мають старішу версію.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При некоректному`mode` викидає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Якщо `tagSets`надається як первинна перевага читання або має неправильний формат (тобто не масив з нуля або більше документів) викидає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Якщо опція `"maxStalenessSeconds"`надається для первинної переваги читання або знаходиться поза діапазоном, викидає[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.8.0 | Добавлен параметр`"hedge"` |
| PECL mongodb 1.3.0 |  |
| Аргумент`mode` тепер набуває рядкового значення, яке відповідає URI-опції `"readPreference"`для[MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.md) |  |

| | PECL mongodb 1.2.0 |

Добавлен третий аргумент`options`, який підтримує параметр `"maxStalenessSeconds"`

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\ReadPreference::\_\_construct()\*\*\*\*

```php
<?php

/* Предпочитать вторичный узел, но в случае отказа отступить к первичному. */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED));

/* Предпочитать узел в Нью-Йоркском центре обработки данных с минимальной задержкой. */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_NEAREST, [['dc' => 'ny']]));

/* Требуется дополнительный узел, чья задержка репликации находится в пределах двух минут от основного */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, ['maxStalenessSeconds' => 120]));

/* Явно включить хеджирование чтения на сервере */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, ['hedge' => ['enabled' => true]]));

?>
```

Результат виконання наведеного прикладу:

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

-   [» Посібник з переваги читання](https://www.mongodb.com/docs/manual/core/read-preference/)
