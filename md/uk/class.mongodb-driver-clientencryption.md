Клас MongoDBDriverClientEncryption

-   [« MongoDBDriverSession::startTransaction](mongodb-driver-session.starttransaction.html)
    
-   [MongoDBDriverClientEncryption::construct »](mongodb-driver-clientencryption.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriver](book.mongodb.html)
    
-   Клас MongoDBDriverClientEncryption
    

# Клас MongoDBDriverClientEncryption

(mongodb >=1.7.0)

## Вступ

Клас **MongoDBDriverClientEncryption** обробляє як створення ключів шифрування за клієнта, і ручне шифрування/дешифрування.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\ClientEncryption
     
     {
    

    
    /* Constants */
    
     const
     string
      AEAD_AES_256_CBC_HMAC_SHA_512_DETERMINISTIC = AEAD_AES_256_CBC_HMAC_SHA_512-Deterministic;

    const
     string
      AEAD_AES_256_CBC_HMAC_SHA_512_RANDOM = AEAD_AES_256_CBC_HMAC_SHA_512-Random;

    const
     string
      ALGORITHM_INDEXED = Indexed;

    const
     string
      ALGORITHM_UNINDEXED = Unindexed;

    const
     string
      QUERY_TYPE_EQUALITY = equality;


    /* Методы */
    
   final public __construct(array $options)
final public createDataKey(string $kmsProvider, ?array $options = null): MongoDB\BSON\Binary
final public decrypt(MongoDB\BSON\Binary $value): mixed
final public encrypt(mixed $value, ?array $options = null): MongoDB\BSON\Binary

   }
```

## Обумовлені константи

**`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_DETERMINISTIC`**

Визначає алгоритм для [» детермінованого шифрування](https://www.mongodb.com/docs/manual/core/security-client-side-encryption/#deterministic-encryption)який підходить для запитів.

**`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_RANDOM`**

Визначає алгоритм для [»¦рандомізованого шифрування](https://www.mongodb.com/docs/manual/core/security-client-side-encryption/#randomized-encryption)

**`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**

Визначає алгоритм для індексованого, зашифрованого корисного навантаження, яке може бути використане з шифруванням з можливістю запиту.

Для додавання або запиту з індексованим, зашифрованим корисним навантаженням [MongoDBDriverManager](class.mongodb-driver-manager.html) має бути налаштований з опцією драйвера `"autoEncryption"`. Опція `"bypassQueryAnalysis"` автоматичне шифрування може бути встановлене як **`true`**. Параметр `"bypassAutoEncryption"` автоматичного шифрування має бути **`false`**

**`MongoDB\Driver\ClientEncryption::ALGORITHM_UNINDEXED`**

Вказує алгоритм для неіндексованого, зашифрованого корисного навантаження.

**`MongoDB\Driver\ClientEncryption::QUERY_TYPE_EQUALITY`**

Визначає тип запиту рівності, який використовується у поєднанні з **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**

> **Зауваження**: Queryable Encryption знаходиться в стадії публічного перегляду і доступний для ознайомлювальних цілей. Його поки що не рекомендується використовувати для розгортань у продакшені, оскільки можуть бути внесені зміни. Додаткову інформацію дивіться у блозі [» Queryable Encryption Preview](https://www.mongodb.com/blog/post/mongodb-releases-queryable-encryption-preview/)

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.14.0 | Додані константи **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`** **`MongoDB\Driver\ClientEncryption::ALGORITHM_UNINDEXED`** і **`MongoDB\Driver\ClientEncryption::QUERY_TYPE_EQUALITY`** |

## Дивіться також

-   [MongoDBDriverManager::createClientEncryption()](mongodb-driver-manager.createclientencryption.html)

## Зміст

-   [MongoDBDriverClientEncryption::construct](mongodb-driver-clientencryption.construct.html) — Створює новий об'єкт ClientEncryption
-   [MongoDBDriverClientEncryption::createDataKey](mongodb-driver-clientencryption.createdatakey.html) — Створює ключ шифрування
-   [MongoDBDriverClientEncryption::decrypt](mongodb-driver-clientencryption.decrypt.html) - Розшифрувати дані
-   [MongoDBDriverClientEncryption::encrypt](mongodb-driver-clientencryption.encrypt.html) - Шифрує дані