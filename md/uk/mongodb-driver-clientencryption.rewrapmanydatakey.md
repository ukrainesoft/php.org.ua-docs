---
navigation:
  - mongodb-driver-clientencryption.removekeyaltname.md: '« MongoDB\\Driver\\ClientEncryption::removeKeyAltName'
  - class.mongodb-driver-serverapi.md: MongoDB\\Driver\\ServerApi »
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::rewrapManyDataKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::rewrapManyDataKey

(mongodb >=1.15.0)

MongoDB\\Driver\\ClientEncryption::rewrapManyDataKey — Перевертає ключі даних

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::rewrapManyDataKey(array|object $filter, ?array $options = null): object
```

Перевертає (тобто розшифровує та заново шифрує) нуль або більше ключів даних у колекції сховища ключів, які відповідають заданому фільтру (`filter`

Якщо опція `"provider"` не вказано, що збігаються ключі даних будуть повторно зашифровані за допомогою поточного постачальника KMS. В іншому випадку ключі даних, що збігаються, будуть зашифровані заново відповідно до зазначених опцій `"provider"`и`"masterKey"`

### Список параметрів

`filter`(array|object)

[» Предикат запиту](https://www.mongodb.com/docs/manual/tutorial/query-documents/). Порожній предикат збігатиметься з усіма елементами колекції.

> **Зауваження**: При обчисленні критеріїв запиту MongoDB порівнює типи та значення відповідно до власних [» правилами порівняння типів BSON](https://www.mongodb.com/docs/manual/reference/bson-type-comparison-order/), відмінних від правил [порівняння](types.comparisons.md) і [приведення типів](language.types.type-juggling.md) PHP. Коли вказано спеціальний тип BSON, критерій запиту має відповідати [класу BSON](book.bson.md) (тобто використовувати [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md) для вибірки по [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)

`options`

**Параметри RewrapManyDataKey**

| Параметр | Тип | Опис |
| --- | --- | --- |
| provider | string |  |
| Провайдер KMS (наприклад, `"local"` `"aws"`), який буде використовуватися для повторного шифрування ключів даних, що збіглися. |  |  |

Якщо провайдер KMS не вказано, то ключі даних, що збігаються, будуть повторно зашифровані за допомогою поточного провайдера KMS.

| | masterKey | array |

Параметр masterKey визначає специфічний для KMS ключ, який використовується для шифрування нового ключа даних. Параметр не повинен вказуватись без параметра `"provider"`Параметр необходим, если указан`"provider"`, а не`"local"`

**Параметри провайдера `"aws"`**

| Параметр | Тип | Опис |
| --- | --- | --- |
| region | Рядок | Обов'язковий. |
| key | Рядок | Обов'язковий. Ім'я ресурсу Amazon (ARN) для ключового ключа клієнта AWS (CMK). |
| endpoint | Рядок | Необов'язковий. Альтернативний ідентифікатор хоста для надсилання запитів KMS. Може містити номер порту. |

**Параметри провайдера `"azure"`**

| Параметр | Тип | Опис |
| --- | --- | --- |
| keyVaultEndpoint | Рядок | Обов'язковий. Хост із необов'язковим портом (наприклад, "example.vault.azure.net"). |
| keyName | Рядок | Обов'язковий. |
| keyVersion | Рядок | Необов'язковий. Певна версія іменованого ключа. За промовчанням – первинна версія ключа. |

**Параметри провайдера `"gcp"`**

| Параметр | Тип | Опис |
| --- | --- | --- |
| projectId | Рядок | Обов'язковий. |
| location | Рядок | Обов'язковий. |
| keyRing | Рядок | Обов'язковий. |
| keyName | Рядок | Обов'язковий. |
| keyVersion | Рядок | Необов'язковий. Певна версія іменованого ключа. За промовчанням – первинна версія ключа. |
| endpoint | Рядок | Необов'язковий. Хост із додатковим портом. За промовчанням "cloudkms.googleapis.com".. |

**Параметри провайдера `"kmip"`**

| Параметр | Тип | Опис |
| --- | --- | --- |
| keyId | Рядок | Необов'язковий. Унікальний ідентифікатор 96-байтового керованого об'єкта секретних даних KMIP. Якщо не вказано, драйвер створює випадковий 96-байтовий керований об'єкт секретних даних KMIP. |
| endpoint | Рядок | Необов'язковий. Хост із додатковим портом. |

### Значення, що повертаються

Повертає об'єкт, який матиме необов'язкову властивість `bulkWriteResult`, содержащее результат внутренней операции`bulkWrite` як об'єкта. Якщо жоден ключ даних не відповідає фільтру або запис не був визнаний, властивість `bulkWriteResult` буде одно **`null`**

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\EncryptionException](class.mongodb-driver-exception-encryptionexception.md), якщо при розшифруванні або повторному шифруванні ключа даних виникла помилка.
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)у разі виникнення інших помилок.
