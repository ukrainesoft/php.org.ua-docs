---
navigation:
  - mongodb-driver-readpreference.unserialize.md: '« MongoDB\\Driver\\ReadPreference::unserialize'
  - mongodb-driver-readconcern.bsonserialize.md: 'MongoDB\\Driver\\ReadConcern::bsonSerialize »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\ReadConcern
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\ReadConcern

(mongodb >=1.1.0)

## Вступ

**MongoDB\\Driver\\ReadConcern** контролює рівень ізоляції для операцій читання для наборів реплік та сегментів наборів реплік. Ця опція потребує MongoDB 3.2 або новіше.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\ReadConcern
     

     implements 
       MongoDB\BSON\Serializable,  Serializable {
    
    /* Константы */
    
     const
     string
      AVAILABLE = "available";

    const
     string
      LINEARIZABLE = "linearizable";

    const
     string
      LOCAL = "local";

    const
     string
      MAJORITY = "majority";

    const
     string
      SNAPSHOT = "snapshot";


    /* Методы */
    
   final public bsonSerialize(): stdClass
final public __construct(?string $level = null)
final public getLevel(): ?string
final public isDefault(): bool
final public serialize(): string
final public unserialize(string $data): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\ReadConcern::AVAILABLE`**

За замовчуванням для читання проти вторинних, коли `afterClusterTime`и`level` не вказані.

Запит повертає останні дані екземпляра. Не гарантує, що дані були записані більшості членів набору реплік (тобто можуть бути відкочені).

Для колекцій, що не охороняються (включаючи колекції в автономному розгортанні або розгортанні набору реплік), `"local"`и`"available"` гарантії читання поводяться однаково.

Для сегментированного кластера`"available"` гарантії читання забезпечує більшу толерантність для розділів, оскільки вона не очікує гарантій узгодженості. Однак запит з `"available"` гарантіями читання може повернути втрачені документи, якщо у сегменті виконується міграція фрагментів, оскільки `"available"`гарантий чтения, в отличие от`"local"` гарантій читання, що не пов'язується з первинним сервером сегмента або серверами конфігурації для отримання оновлених метаданих.

**`MongoDB\Driver\ReadConcern::LINEARIZABLE`**

Запит повертає дані, які відображають усі успішні записи, випущені з гарантіями запису `"majority"` *і* підтверджені на початок операції читання. Для наборів реплік, які виконуються з параметром `writeConcernMajorityJournalDefault`, встановленим у значення \*\*`true`\*\*лінеаризовані гарантії читання повертають дані, які ніколи не будуть відкочуватися.

Якщо для `writeConcernMajorityJournalDefault`задано значение\*\*`false`\*\*, MongoDB не буде очікувати `w: "majority"` записів буде стійким, перш ніж підтвердити запис. Таким чином, операції запису `"majority"` можуть відкочуватися у разі втрати члена набору реплік.

Ви можете вказати лінеаризовані гарантії читання для операцій читання лише на основному сервері.

Лінеаризовані гарантії читання застосовуються лише в тому випадку, якщо в операціях читання вказано фільтр запиту, який однозначно ідентифікує один документ.

**Підказка**

Всегда используйте`maxTimeMS` з лінеаризованими гарантіями читання, якщо більшість елементів, що несуть дані, недоступні . `maxTimeMS` гарантує, що операція не блокується нескінченно, і натомість гарантує, що операція повертає помилку, якщо проблема читання може бути виконана.

Для лінеаризованих гарантій читання потрібен MongoDB 3.4.

**`MongoDB\Driver\ReadConcern::LOCAL`**

За промовчанням для читання по первинному, якщо `level` не вказано, і для читання з вторинного, якщо `level` не вказано, але встановлено `afterClusterTime`

Запит повертає останні дані екземпляра. Не гарантує, що дані були записані більшості членів набору реплік (тобто можуть бути відкочені).

**`MongoDB\Driver\ReadConcern::MAJORITY`**

Запит повертає останні дані екземпляра, які були визнані записаними більшості членів у наборі реплік.

Щоб використати рівень гарантій читання `"majority"`, набори реплік повинні використовувати механізм зберігання WiredTiger та протокол вибору версії 1.

**`MongoDB\Driver\ReadConcern::SNAPSHOT`**

Гарантія читання `"snapshot"` доступна для транзакцій з кількома документами, а починаючи з MongoDB 5.0, також доступна для деяких операцій читання не тільки для транзакцій з кількома документами.

Якщо транзакція не є частиною причинно-узгодженої сесії, після фіксації транзакції з проблемою запису `"majority"`, операції транзакції гарантовано прочитають з моментального знімку зафіксованих більшістю даних.

Якщо транзакція є частиною причинно-узгодженої сесії, при фіксації транзакції із проблемою запису `"majority"`, операції транзакції гарантовано зчитують з моментального знімку дані, підтверджені більшістю, що забезпечує причинну узгодженість операцій, безпосередньо попередньої початку транзакції.

Поза транзакціями з кількома документами, проблема читання `"snapshot"` доступна на первинних та вторинних серверах для наступних операцій читання: `find` `aggregate`и`distinct` (Для необроблених колекцій). Усі інші команди читання забороняють `"snapshot"`

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.11.0 |  |
| Добавлена константа\*\*`MongoDB\Driver\ReadConcern::SNAPSHOT`\*\* |  |

| | PECL mongodb 1.7.0 | Реализует[Serializable](class.serializable.md)| | PECL mongodb 1.4.0 |

Добавлена константа\*\*`MongoDB\Driver\ReadConcern::AVAILABLE`\*\*

| | PECL mongodb 1.2.0 |

Добавлена константа\*\*`MongoDB\Driver\ReadConcern::LINEARIZABLE`\*\*

Реалізує [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.md)

## Дивіться також

-   [» Довідка за гарантіями читання](https://www.mongodb.com/docs/manual/reference/read-concern/)

## Зміст

-   [MongoDB\\Driver\\ReadConcern::bsonSerialize](mongodb-driver-readconcern.bsonserialize.md)— Повертає об'єкт для серіалізації BSON
-   [MongoDB\\Driver\\ReadConcern::\_\_construct](mongodb-driver-readconcern.construct.md) \- Створює новий ReadConcern
-   [MongoDB\\Driver\\ReadConcern::getLevel](mongodb-driver-readconcern.getlevel.md) - Повертає опцію "level" ReadConcern
-   [MongoDB\\Driver\\ReadConcern::isDefault](mongodb-driver-readconcern.isdefault.md)— Перевіряє, чи є гарантією прочитання за умовчанням
-   [MongoDB\\Driver\\ReadConcern::serialize](mongodb-driver-readconcern.serialize.md) \- Серіалізація ReadConcern
-   [MongoDB\\Driver\\ReadConcern::unserialize](mongodb-driver-readconcern.unserialize.md) \- Десеріалізація ReadConcern
