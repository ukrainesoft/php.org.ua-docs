---
navigation:
  - mongodb-driver-manager.construct.md: '« MongoDB\\Driver\\Manager::\_\_construct'
  - mongodb-driver-manager.executebulkwrite.md: 'MongoDB\\Driver\\Manager::executeBulkWrite »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::createClientEncryption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::createClientEncryption

(mongodb >=1.7.0)

MongoDB\\Driver\\Manager::createClientEncryption — Створення нового об'єкта ClientEncryption

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::createClientEncryption(array $options): MongoDB\Driver\ClientEncryption
```

Створює новий об'єкт [MongoDB\\Driver\\ClientEncryption](class.mongodb-driver-clientencryption.md) із заданими параметрами.

### Список параметрів

`options`

**options**

| Параметр | Тип | Опис |
| --- | --- | --- |
| keyVaultClient | [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md) | Менеджер маршрутизації запитів ключів даних окремий кластер MongoDB. За замовчуванням метод вибирає поточний менеджер та кластер. |
| keyVaultNamespace | string | Повний простір імен (наприклад, `"databaseName.collectionName"`), що означає колекцію, яка містить усі ключі даних, що використовуються для шифрування та дешифрування. Обов'язковий параметр. |
| kmsProviders | array |  |
| Документ, який містить конфігурацію для одного або кількох провайдерів KMS, які використовуються для шифрування ключів даних. Підтримуються провайдери `"aws"` `"azure"` `"gcp"`и`"local"`, і принаймні один з них повинен бути вказаний. |  |  |

Якщо для `"aws"` `"azure"`или`"gcp"` вказано порожній документ, драйвер спробує налаштувати провайдера, використовуючи [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

Формат для`"aws"` виглядає наступним чином:

aws: { accessKeyId:, secretAccessKey:, sessionToken:}

Формат для`"azure"` виглядає наступним чином:

azure: { tenantId:, clientId:, clientSecret:, identityPlatformEndpoint: // За замовчуванням "login.microsoftonline.com"

}

Формат для`"gcp"` виглядає наступним чином:

gcp: { email:, privateKey:|<MongoDB\\BSON\\Binary>, endpoint: // За замовчуванням "oauth2.googleapis.com"

}

Формат для`"kmip"` виглядає наступним чином:

kmip: { endpoint:}

Формат для`"local"` виглядає наступним чином:

local: { // 96-байтовий головний ключ, який використовується для шифрування/дешифрування ключів даних key: |<MongoDB\\BSON\\Binary> }

| | tlsOptions | array |

Документ, який містить конфігурацію TLS для одного або кількох KMS провайдерів. Підтримуються провайдери `"aws"` `"azure"` `"gcp"`и`"kmip"`. Усі провайдери підтримують такі опції:

: { tlsCaFile:, tlsCertificateKeyFile:, tlsCertificateKeyFilePassword:, tlsDisableOCSPEndpointCheck:}

### Значення, що повертаються

Повертає новий екземпляр [MongoDB\\Driver\\ClientEncryption](class.mongodb-driver-clientencryption.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)якщо модуль був скомпільований без підтримки libmongocrypt

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.16.0 |  |
| Провайдер AWS KMS для шифрування на стороні клієнта тепер приймає параметр `"sessionToken"`, який можна використовувати для автентифікації з тимчасовими обліковими даними AWS. |  |

Для налаштування `"tlsOptions"`добавлена настройка`"tlsDisableOCSPEndpointCheck"`

Якщо для KMS-провайдерів `"azure"`или`"gcp"` вказано порожній документ, драйвер спробує налаштувати провайдера, заповнивши [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

| | PECL mongodb 1.15.0 |

Якщо для KMS-провайдера `"aws"` вказано порожній документ, драйвер спробує налаштувати провайдера, заповнивши [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

| | PECL mongodb 1.12.0 |

KMIP тепер підтримується як KMS провайдер для шифрування на стороні клієнта і може бути налаштований за допомогою параметра `"kmsProviders"`

Добавлен параметр`"tlsOptions"`

| | PECL mongodb 1.10.0 Azure та GCP тепер підтримуються як постачальники KMS для шифрування на стороні клієнта і можуть бути налаштовані в полі `"kmsProviders"`параметра драйвера`"autoEncryption"`. Рядки в кодуванні Base64 тепер приймаються як альтернатива [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md)для параметров внутри`"kmsProviders"`.

### Дивіться також

-   [MongoDB\\Driver\\ClientEncryption::\_\_construct()](mongodb-driver-clientencryption.construct.md) \- Створює новий об'єкт ClientEncryption
-   Сторінка в посібнику з MongoDB:[» Явне (ручне) шифрування на рівні поля на стороні клієнта](https://www.mongodb.com/docs/manual/core/security-explicit-client-side-encryption/)
