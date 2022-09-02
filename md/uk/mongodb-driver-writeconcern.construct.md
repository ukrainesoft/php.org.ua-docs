---
navigation:
  - mongodb-driver-writeconcern.bsonserialize.md: '« MongoDBDriverWriteConcern::bsonSerialize'
  - mongodb-driver-writeconcern.getjournal.md: 'MongoDBDriverWriteConcern::getJournal »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDBDriverWriteConcern
title: 'MongoDBDriverWriteConcern::construct'
---
# MongoDBDriverWriteConcern::construct

(mongodb >=1.0.0)

MongoDBDriverWriteConcern::construct — Створити новий WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::__construct(string|int $w, ?int $wtimeout = null, ?bool $journal = null)
```

Створює новий [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)що є незмінним об'єктом значення.

### Список параметрів

`w`

**Гарантія запису**

| Значение | Описание |
| --- | --- |
|  | Потребує підтвердження, що операція запису поширилася на автономний `mongod` або на первинний у наборі реплік. Це гарантія запису за промовчанням для MongoDB. |
|  | Не вимагає підтвердження операції запису. Тим не менш, це може повернути інформацію про виключення сокету та мережеві помилки в додаток. |
| <ціле число більше 1> | Числа, що перевищують 1, дійсні тільки для набору реплік для запиту підтвердження від зазначеної кількості членів, включаючи первинний. |
| **`MongoDB\Driver\WriteConcern::MAJORITY`** |  |
| Вимагає підтвердження того, що операції запису поширюються на більшість голосуючих вузлів, включаючи первинний, і записані в журнал на диск для цих вузлів. |  |

До MongoDB 3.0 це стосується більшості членів набору реплік (а не тільки до вузлів голосування).

| | string | Рядкове представлення інтерпретується як набір тегів. Потребує підтвердження, що операція запису поширюється на член набору реплік із зазначеним тегом. |

`wtimeout`

Скільки чекати (у мілісекундах) відповіді від вторинних вузлів перед тим, як видати помилку.

`wtimeout` призводить до того, що операції запису повертаються з помилкою (**WriteConcernError**) після зазначеного періоду, навіть якщо необхідна гарантія запису в кінцевому рахунку буде успішною. Коли ці гарантії запису повертаються, MongoDB не скасовує успішні зміни даних, виконані до того, як гарантія запису перевищила тимчасовий ліміт. `wtimeout`

Якщо зазначено, `wtimeout` повинен бути 64-бітовим цілим числом зі знаком, більшим або рівним нулю.

**Час очікування гарантії запису**

| Значение | Описание |
| --- | --- |
|  | Блокувати нескінченно. Це значення за промовчанням. |
| <ціле число більше, ніж 0> | Мілісекунди до очікування повернення. |

`journal`

Чекати, поки mongod не застосує запис до журналу.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невірному `w` чи негативному `wtimeout` або якщо вони більше, ніж 32-бітове ціле число зі знаком, викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.7.0 | Параметр `wTimeout` тепер набуває 64-бітових значень. |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcern::construct()****

```php
<?php

/* Запрос подтверждения записи от большинства узлов набора реплик */
$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 500);

/* Запрос подтверждения записи от узла, настроенного с тегом "MultipleDC" */
$wc = new MongoDB\Driver\WriteConcern("MultipleDC", 500);

?>
```

### Дивіться також

-   [» Довідкова інформація щодо гарантії запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
