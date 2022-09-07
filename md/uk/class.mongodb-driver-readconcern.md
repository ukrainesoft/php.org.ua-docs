---
navigation:
  - mongodb-driver-readpreference.unserialize.md: '« MongoDBDriverReadPreference::unserialize'
  - mongodb-driver-readconcern.bsonserialize.md: 'MongoDBDriverReadConcern::bsonSerialize »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас MongoDBDriverReadConcern
---
# Клас MongoDBDriverReadConcern

(mongodb >=1.1.0)

## Вступ

**MongoDBDriverReadConcern** контролює рівень ізоляції для операцій читання для наборів реплік та сегментів наборів реплік. Ця опція потребує MongoDB 3.2 або новіше.

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
    
   final public bsonSerialize(): object
final public __construct(?string $level = null)
final public getLevel(): ?string
final public isDefault(): bool
final public serialize(): string
final public unserialize(string $serialized): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\ReadConcern::AVAILABLE`**

За замовчуванням для читання проти вторинних, коли `afterClusterTime` і `level` не вказані.

Запит повертає останні дані екземпляра. Не гарантує, що дані були записані більшості членів набору реплік (тобто можуть бути відкати).

Для колекцій, що не охороняються (включаючи колекції в автономному розгортанні або розгортанні набору реплік), `"local"` і `"available"` гарантії читання поводяться однаково.

Для сегментованого кластера `"available"` гарантії читання забезпечує більшу толерантність для розділів, оскільки вона не очікує гарантій узгодженості. Однак запит з `"available"` гарантіями читання може повернути втрачені документи, якщо в сегменті виконується міграція фрагментів, оскільки `"available"` гарантій читання, на відміну від `"local"` гарантій читання, що не пов'язується з первинним сервером сегмента або серверами конфігурації для отримання оновлених метаданих.

**`MongoDB\Driver\ReadConcern::LINEARIZABLE`**

Запит повертає дані, які відображають усі успішні записи, випущені з гарантіями запису `"majority"` *і* підтверджені на початок операції читання. Для наборів реплік, які виконуються з параметром `writeConcernMajorityJournalDefault`, встановленим у значення \*\*`true`\*\*лінеаризовані гарантії читання повертають дані, які ніколи не будуть відкочуватися.

Якщо для `writeConcernMajorityJournalDefault` встановлено значення **`false`**, MongoDB не буде очікувати `w: "majority"` записів буде стійким, перш ніж підтвердити запис. Таким чином, операції запису `"majority"` можуть відкочуватися у разі втрати члена набору реплік.

Ви можете вказати лінеаризовані гарантії читання для операцій читання лише на основному сервері.

Лінеаризовані гарантії читання застосовуються лише в тому випадку, якщо в операціях читання вказано фільтр запиту, який однозначно ідентифікує один документ.

**Підказка**

Завжди використовуйте `maxTimeMS` з лінеаризованими гарантіями читання, якщо більшість елементів, що несуть дані, недоступні . `maxTimeMS` гарантує, що операція не блокується нескінченно, і натомість гарантує, що операція повертає помилку, якщо проблема читання може бути виконана.

Для лінеаризованих гарантій читання потрібен MongoDB 3.4.

**`MongoDB\Driver\ReadConcern::LOCAL`**

За промовчанням для читання по первинному, якщо `level` не вказано, і для читання з вторинного, якщо `level` не вказано, але встановлено `afterClusterTime`

Запит повертає останні дані екземпляра. Не гарантує, що дані були записані більшості членів набору реплік (тобто можуть бути відкати).

**`MongoDB\Driver\ReadConcern::MAJORITY`**

Запит повертає останні дані екземпляра, які були визнані записаними більшості членів у наборі реплік.

Щоб використати рівень гарантій читання `"majority"`, набори реплік повинні використовувати механізм зберігання WiredTiger та протокол вибору версії 1.

**`MongoDB\Driver\ReadConcern::SNAPSHOT`**

Гарантія читання `"snapshot"` доступна для транзакцій з кількома документами, а починаючи з MongoDB 5.0, також доступна для деяких операцій читання не тільки для транзакцій з кількома документами.

Якщо транзакція не є частиною причинно-узгодженої сесії, після фіксації транзакції з проблемою запису `"majority"`, операції транзакції гарантовано прочитають з моментального знімку зафіксованих більшістю даних.

Якщо транзакція є частиною причинно-узгодженої сесії, при фіксації транзакції із проблемою запису `"majority"`, операції транзакції гарантовано зчитують з моментального знімку дані, підтверджені більшістю, що забезпечує причинну узгодженість операцій, безпосередньо попередньої початку транзакції.

Поза транзакціями з кількома документами, проблема читання `"snapshot"` доступна на первинних та вторинних серверах для наступних операцій читання: `find` `aggregate` і `distinct` (Для необроблених колекцій). Усі інші команди читання забороняють `"snapshot"`

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.11.0 |  |
| Додано константу **`MongoDB\Driver\ReadConcern::SNAPSHOT`** |  |

| | PECL mongodb 1.7.0 Реалізує [Serializable](class.serializable.md). | | PECL mongodb 1.4.0

Додано константу **`MongoDB\Driver\ReadConcern::AVAILABLE`**

| | PECL mongodb 1.2.0

Додано константу **`MongoDB\Driver\ReadConcern::LINEARIZABLE`**

Реалізує [MongoDBBSONSerializable](class.mongodb-bson-serializable.md)

## Дивіться також

-   [» Справка по гарантиям чтения](https://www.mongodb.com/docs/manual/reference/read-concern/)

## Зміст

-   [MongoDBDriverReadConcern::bsonSerialize](mongodb-driver-readconcern.bsonserialize.md) — Повертає об'єкт для серіалізації BSON
-   [MongoDBDriverReadConcern::construct](mongodb-driver-readconcern.construct.md) - Створює новий ReadConcern
-   [MongoDBDriverReadConcern::getLevel](mongodb-driver-readconcern.getlevel.md) - Повертає опцію "level" ReadConcern
-   [MongoDBDriverReadConcern::isDefault](mongodb-driver-readconcern.isdefault.md) — Перевіряє, чи є гарантією прочитання за умовчанням
-   [MongoDBDriverReadConcern::serialize](mongodb-driver-readconcern.serialize.md) - Серіалізація ReadConcern
-   [MongoDBDriverReadConcern::unserialize](mongodb-driver-readconcern.unserialize.md) - Десеріалізація ReadConcern
