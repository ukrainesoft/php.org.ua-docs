---
navigation:
  - class.mongodb-driver-query.md: « MongoDB\\Driver\\Query
  - class.mongodb-driver-bulkwrite.md: MongoDB\\Driver\\BulkWrite »
  - index.md: PHP Manual
  - class.mongodb-driver-query.md: MongoDB\\Driver\\Query
title: 'MongoDB\\Driver\\Query::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Query::\_\_construct

(mongodb >=1.0.0)

MongoDB\\Driver\\Query::\_\_construct — Створює новий запит

### Опис

```methodsynopsis
final public MongoDB\Driver\Query::__construct(array|object $filter, ?array $queryOptions = null)
```

Створює новий [MongoDB\\Driver\\Query](class.mongodb-driver-query.md)який є об'єктом незмінного значення, що представляє запит до бази даних. Потім запит може бути виконаний за допомогою [MongoDB\\Driver\\Manager::executeQuery()](mongodb-driver-manager.executequery.md)

### Список параметрів

`filter`(array|object)

[» Предикат запиту](https://www.mongodb.com/docs/manual/tutorial/query-documents/). Порожній предикат збігатиметься з усіма елементами колекції.

> **Зауваження**: При обчисленні критеріїв запиту MongoDB порівнює типи та значення відповідно до власних [» правилами порівняння типів BSON](https://www.mongodb.com/docs/manual/reference/bson-type-comparison-order/), відмінних від правил [порівняння](types.comparisons.md) і [приведення типів](language.types.type-juggling.md) PHP. Коли вказано спеціальний тип BSON, критерій запиту має відповідати [класу BSON](book.bson.md) (тобто використовувати [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md) для вибірки по [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)

`queryOptions`

**queryOptions**

| Опция | Тип | Опис |
| --- | --- | --- |
| allowDiskUse | bool |  |
| Дозволяє MongoDB використовувати тимчасові файли на диску для зберігання даних, що перевищують межу системної пам'яті 100 мегабайт, при обробці операції сортування блокування. |  |  |

| | allowPartialResults | bool |

Для запитів до ізольованої колекції повертає часткові результати з mongos, якщо деякі шарди недоступні замість видачі помилки.

Возврат к устаревшей`"partial"` опції, якщо вона не вказана.

| | awaitData | bool | Використовуйте разом із опцією `"tailable"`тимчасово заблокувати операцію getMore для курсору, якщо в кінці даних, а не повертати жодних даних. Після закінчення часу очікування запит повертається, як завжди. | | batchSize | int |

Кількість документів для повернення у першому пакеті. За замовчуванням – 101. Розмір пакета 0 означає, що курсор буде встановлений, але жодні документи не будуть повернуті у першому пакеті.

У версіях MongoDB до 3.2, де запити використовують застарілий дротовий протокол OP\_QUERY, розмір пакета, що дорівнює 1, буде закривати курсор незалежно від кількості документів, що збігаються.

| | collation | array|object |

[» Зіставлення](https://www.mongodb.com/docs/upcoming/reference/collation/) дозволяє користувачам вказувати специфічні для конкретної мови правила для порівняння рядків, такі як реакцію на регістр літер та надрядкові знаки. Якщо поставлено зіставлення, то поле `"locale"`также обязательно. Опис полей смотрите в разделе[» Зіставлення](https://www.mongodb.com/docs/upcoming/reference/collation/#collation-document)

Якщо зіставлення не задано явно, але в колекції визначено зіставлення за умовчанням, буде використано воно. Якщо немає ні того, то MongoDB буде використовувати просте бінарне порівняння рядків.

Ця опція доступна у MongoDB 3.4+ і, якщо буде використана для більш старих версій, викличе виняток під час виконання.

| | comment |[mixed](language.types.declarations.md#language.types.declarations.mixed)

Довільний коментар, що допомагає відстежити операцію за допомогою профільника бази даних, виводу CurrentOp та журналів.

Коментар може бути будь-яким типом BSON для MongoDB 4.4+. Більш ранні версії сервера підтримують лише строкові значення.

Возврат к устаревшему модификатору`"$comment"`якщо він не вказаний.

| | exhaust | bool |

Потокова передача даних на повну потужність в декількох "додаткових" пакетах за умови, що клієнт повністю прочитає всі дані, що запитуються. Швидше, коли ви отримуєте багато даних і знаєте, що ви хочете все це перенести. Примітка: клієнт не має права не читати всі дані, якщо не закриває з'єднання.

Ця опція не підтримується командою find у MongoDB 3.2+ і змусить драйвер використовувати застарілу версію проводового протоколу (тобто OP\_QUERY).

| | explain | bool |

Якщо **`true`**, повернутий [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md) міститиме один документ, який описує процес та індекси, що використовуються для повернення запиту.

Возврат к устаревшему модификатору`"$explain"`якщо він не вказаний.

Ця опція не підтримується командою find в MongoDB 3.2+ і враховуватиметься лише при використанні застарілої версії проводового протоколу (тобто OP\_QUERY). Команда[» explain](https://www.mongodb.com/docs/manual/reference/command/explain/) має використовуватися на MongoDB 3.0+.

| | hint | string|array|object |

Індекс специфікації. Вкажіть або назву індексу у вигляді рядка, або шаблон ключа індексу. Якщо вказано, то система запитів розглядатиме плани лише з використанням індексу хінтованого.

Откат к устаревшей опции`"hint"`якщо вона не вказана.

| | let | array|object |

Карта імен та значень параметрів. Значення мають бути константами або закритими виразами, які посилаються на поля документа. До параметрів можна звертатися як до змінних у контексті агрегованого виразу (наприклад, `$$var`

Опція доступна в MongoDB 5.0+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | limit | int |

Максимальна кількість документів для повернення. Якщо не вказано, використовується за умовчанням без обмежень. Значення 0 еквівалентне встановленню без обмеження.

Негативне значення інтерпретуватиметься як позитивне значення з параметром `"singleBatch"`, встановленим у значення **`true`**. Ця поведінка підтримується для зворотної сумісності, але її слід вважати застарілою.

| | max | array|object |

*Ексклюзивна* верхня межа для певного індексу.

Возврат к устаревшему модификатору`"$max"`якщо він не вказаний.

| | maxAwaitTimeMS | int |

Позитивне ціле число, що означає обмеження часу в мілісекундах для сервера, щоб заблокувати операцію getMore, якщо дані недоступні. Ця опція повинна використовуватися лише у поєднанні з опціями `"tailable"`и`"awaitData"`

| | maxScan | int |

**Увага**

Ця опція застаріла і не повинна використовуватись.

Ціла позитивна кількість, що позначає максимальну кількість документів або індексних ключів для сканування при виконанні запиту.

Возврат к устаревшему модификатору`"$maxScan"`якщо він не вказаний.

| | maxTimeMS | int |

Накопичений ліміт часу у мілісекундах для операцій обробки на курсорі. MongoDB перериває операцію в найближчій точці переривання.

Возврат к устаревшему модификатору`"$maxTimeMS"`якщо він не вказаний.

| | min | array|object |

*Включає* нижня межа для певного індексу.

Возврат к устаревшему модификатору`"$min"`якщо він не вказаний.

| | modifiers | array |[» Метаоператори](https://www.mongodb.com/docs/manual/reference/operator/query-modifier/), що змінюють виведення чи поведінку запиту. Використання цих операторів не рекомендується на користь іменованих опцій. | | noCursorTimeout | bool | Забороняє серверу синхронізувати незайняті курсори після періоду бездіяльності (10 хвилин). | | oplogReplay | bool |

Внутрішнє використання для реплік наборів. Щоб використовувати oplogReplay, ви повинні включити до фільтра наступну умову:

\[ 'ts' => \[ '$gte' => \] \]

> **Зауваження**: Опція застаріла з версії 1.8.0

| | projection | array|object |

[» Специфікація проекції](https://www.mongodb.com/docs/manual/tutorial/project-fields-from-query-results/) для визначення полів, які необхідно включити до документів, що повертаються.

Якщо ви використовуєте [функцію ODM](mongodb.persistence.deserialization.md) для десеріалізації документів як їх вихідний клас PHP, переконайтеся, що ви включили поле \_\_pclass у проекцію. Це необхідно для роботи десеріалізації, і без неї драйвер поверне (за умовчанням) об'єкт [stdClass](class.stdclass.md)

| | readConcern |[MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)

Гарантії читання застосувати до операції. За промовчанням будуть використовуватися гарантії читання з [URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказано для старої версії сервера.

| | returnKey | bool |

Якщо **`true`**, повертає лише індексні ключі у результуючих документах. Значення за умовчанням є **`false`**. Якщо **`true`** і команда find не використовують індекс, повернуті документи будуть порожніми.

Возврат к устаревшему модификатору`"$returnKey"`якщо він не вказаний.

| | showRecordId | bool |

Визначає, чи повертати ідентифікатор запису для кожного документа. Якщо **`true`**, добавляет поле`"$recordId"` верхнього рівня до повернутих документів.

Возврат к устаревшему модификатору`"$showDiskLoc"`якщо він не вказаний.

| | singleBatch | bool | Визначає, чи закривати курсор після першого пакета. За замовчуванням **`false`**| | skip | int | Количество документов для пропуска. По умолчанию 0. | | snapshot | bool |

**Увага**

Ця опція застаріла і не повинна використовуватись.

Забороняє курсору повертати документ більше одного разу через проміжну операцію запису.

Возврат к устаревшему модификатору`"$snapshot"`якщо він не вказаний.

| | sort | array|object |

Специфікація сортування для впорядкування результатів.

Возврат к устаревшему модификатору`"$orderby"`якщо він не вказаний.

| | tailable | bool | Повертає курсор для обмеженої колекції. |

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.14.0 |  |
| Добавлена опция`"let"`Опция`"comment"` тепер приймає будь-який тип. |  |

| | PECL mongodb 1.8.0 |

Добавлен параметр`"allowDiskUse"`

Параметр`"oplogReplay"` оголошено застарілим.

| | PECL mongodb 1.5.0 |

Параметри `"maxScan"`и`"snapshot"`устарели.

| | PECL mongodb 1.3.0 |

Добавлен параметр`"maxAwaitTimeMS"`

| | PECL mongodb 1.2.0 |

Добавлен параметр`"allowPartialResults"` `"collation"` `"comment"` `"hint"` `"max"` `"maxScan"` `"maxTimeMS"` `"min"` `"returnKey"` `"showRecordId"`, и`"snapshot"`

Переименован параметр`"partial"`в`"allowPartialResults"`. Для зворотної сумісності, `"partial"` все одно буде прочитаний, якщо `"allowPartialResults"` не вказано.

Видалено застарілий параметр `"secondaryOk"`. Для запитів, які використовують застарілий дротовий протокол OP\_QUERY, драйвер установит бит`secondaryOk` при необхідності відповідно до [» Специфікацією вибору сервера](https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst)

| | PECL mongodb 1.1.0 | Добавлен параметр`"readConcern"`.

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Query::\_\_construct()\*\*\*\*

```php
<?php
/* Выберите только документы, автором которых является "bjori" с не менее 100 просмотров */
$filter = [
    'author' => 'bjori',
    'views' => [
        '$gte' => 100,
    ],
];

$options = [
    /* Вернуть только следующие поля в соответствующих документах */
    'projection' => [
        'title' => 1,
        'article' => 1,
    ],
    /* Вернуть документы в порядке убывания просмотров */
    'sort' => [
        'views' => -1
    ],
];

$query = new MongoDB\Driver\Query($filter, $options);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$readPreference = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$cursor = $manager->executeQuery('databaseName.collectionName', $query, $readPreference);

foreach($cursor as $document) {
    var_dump($document);
}

?>
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::executeQuery()](mongodb-driver-manager.executequery.md) \- Виконує запит до бази даних
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)
