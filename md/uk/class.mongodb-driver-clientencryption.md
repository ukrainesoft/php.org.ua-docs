---
navigation:
  - mongodb-driver-session.starttransaction.md: '« MongoDB\\Driver\\Session::startTransaction'
  - mongodb-driver-clientencryption.addkeyaltname.md: 'MongoDB\\Driver\\ClientEncryption::addKeyAltName »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\ClientEncryption
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\ClientEncryption

(mongodb >=1.7.0)

## Вступ

Класс**MongoDB\\Driver\\ClientEncryption** обробляє як створення ключів шифрування за клієнта, і ручне шифрування/дешифрування.

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
      ALGORITHM_RANGE_PREVIEW = RangePreview;

    const
     string
      QUERY_TYPE_EQUALITY = equality;

    const
     string
      QUERY_TYPE_RANGE_PREVIEW = rangePreview;


    /* Методы */
    
   final public addKeyAltName(MongoDB\BSON\Binary $keyId, string $keyAltName): ?object
final public __construct(array $options)
final public createDataKey(string $kmsProvider, ?array $options = null): MongoDB\BSON\Binary
final public decrypt(MongoDB\BSON\Binary $value): mixed
final public deleteKey(MongoDB\BSON\Binary $keyId): object
final public encrypt(mixed $value, ?array $options = null): MongoDB\BSON\Binary
final public encryptExpression(array|object $expr, ?array $options = null): object
final public getKey(MongoDB\BSON\Binary $keyId): ?object
final public getKeyByAltName(string $keyAltName): ?object
final public getKeys(): MongoDB\Driver\Cursor
final public removeKeyAltName(MongoDB\BSON\Binary $keyId, string $keyAltName): ?object
final public rewrapManyDataKey(array|object $filter, ?array $options = null): object

   }
```

## Обумовлені константи

**`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_DETERMINISTIC`**

Визначає алгоритм для [» детермінованого шифрування](https://www.mongodb.com/docs/manual/core/security-client-side-encryption/#deterministic-encryption)який підходить для запитів.

**`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_RANDOM`**

Визначає алгоритм для [»¦рандомізованого шифрування](https://www.mongodb.com/docs/manual/core/security-client-side-encryption/#randomized-encryption)

**`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**

Визначає алгоритм для індексованого, зашифрованого корисного навантаження, яке може бути використане з шифруванням з можливістю запиту.

Для додавання або запиту з індексованим, зашифрованим корисним навантаженням [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md) має бути налаштований з опцією драйвера `"autoEncryption"`Опция`"bypassQueryAnalysis"` автоматичне шифрування може бути встановлене як \*\*`true`\*\*Параметр`"bypassAutoEncryption"` автоматичного шифрування має бути **`false`**

**`MongoDB\Driver\ClientEncryption::ALGORITHM_UNINDEXED`**

Вказує алгоритм для неіндексованого, зашифрованого корисного навантаження.

**`MongoDB\Driver\ClientEncryption::ALGORITHM_RANGE_PREVIEW`**

Визначає алгоритм для діапазону зашифрованого корисного навантаження, яке може бути використане з шифруванням з можливістю запиту.

Для виконання запиту із зашифрованим корисним навантаженням діапазону [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md) має бути налаштований з опцією драйвера `"autoEncryption"`Опция`"bypassQueryAnalysis"` автоматичного шифрування може бути \*\*`true`\*\*Параметр`"bypassAutoEncryption"` автоматичного шифрування має бути **`false`**

> **Зауваження** :
> 
> Алгоритм діапазону є експериментальним. Він призначений для громадського використання.
> 
> Драйвер PHP поки не підтримує запити діапазону типів полів decimal128 BSON.

**`MongoDB\Driver\ClientEncryption::QUERY_TYPE_EQUALITY`**

Визначає тип запиту рівності, який використовується у поєднанні з **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**

**`MongoDB\Driver\ClientEncryption::QUERY_TYPE_RANGE_PREVIEW`**

Задає тип запиту діапазону, який використовується у поєднанні з **`MongoDB\Driver\ClientEncryption::ALGORITHM_RANGE_PREVIEW`**

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.16.0 | Додані константи **`MongoDB\Driver\ClientEncryption::ALGORITHM_RANGE_PREVIEW`**и**`MongoDB\Driver\ClientEncryption::QUERY_TYPE_RANGE_PREVIEW`** |
| PECL mongodb 1.14.0 | Додані константи **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`** **`MongoDB\Driver\ClientEncryption::ALGORITHM_UNINDEXED`**и**`MongoDB\Driver\ClientEncryption::QUERY_TYPE_EQUALITY`** |

## Дивіться також

-   [MongoDB\\Driver\\Manager::createClientEncryption()](mongodb-driver-manager.createclientencryption.md)

## Зміст

-   [MongoDB\\Driver\\ClientEncryption::addKeyAltName](mongodb-driver-clientencryption.addkeyaltname.md)— Додає альтернативне ім'я до документа із ключем
-   [MongoDB\\Driver\\ClientEncryption::\_\_construct](mongodb-driver-clientencryption.construct.md)— Створює новий об'єкт ClientEncryption
-   [MongoDB\\Driver\\ClientEncryption::createDataKey](mongodb-driver-clientencryption.createdatakey.md)— Створює документ із ключем
-   [MongoDB\\Driver\\ClientEncryption::decrypt](mongodb-driver-clientencryption.decrypt.md) \- Розшифрувати дані
-   [MongoDB\\Driver\\ClientEncryption::deleteKey](mongodb-driver-clientencryption.deletekey.md)— Видаляє документ із ключем
-   [MongoDB\\Driver\\ClientEncryption::encrypt](mongodb-driver-clientencryption.encrypt.md) \- Шифрує дані
-   [MongoDB\\Driver\\ClientEncryption::encryptExpression](mongodb-driver-clientencryption.encryptexpression.md)— Шифрує збіг чи агрегований вираз
-   [MongoDB\\Driver\\ClientEncryption::getKey](mongodb-driver-clientencryption.getkey.md)— Отримує документ із ключем
-   [MongoDB\\Driver\\ClientEncryption::getKeyByAltName](mongodb-driver-clientencryption.getkeybyaltname.md)— Отримує документ із ключем щодо альтернативного імені
-   [MongoDB\\Driver\\ClientEncryption::getKeys](mongodb-driver-clientencryption.getkeys.md)— Отримує всі документи із ключем
-   [MongoDB\\Driver\\ClientEncryption::removeKeyAltName](mongodb-driver-clientencryption.removekeyaltname.md)— Видаляє альтернативне ім'я з документа із ключем
-   [MongoDB\\Driver\\ClientEncryption::rewrapManyDataKey](mongodb-driver-clientencryption.rewrapmanydatakey.md)— Перевертає ключі даних
