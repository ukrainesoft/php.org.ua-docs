---
navigation:
  - mongodb-driver-clientencryption.addkeyaltname.md: '« MongoDB\\Driver\\ClientEncryption::addKeyAltName'
  - mongodb-driver-clientencryption.createdatakey.md: 'MongoDB\\Driver\\ClientEncryption::createDataKey »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::\_\_construct

(mongodb >=1.14.0)

MongoDB\\Driver\\ClientEncryption::\_\_construct — Створює новий об'єкт ClientEncryption

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::__construct(array $options)
```

Створює новий об'єкт [MongoDB\\Driver\\ClientEncryption](class.mongodb-driver-clientencryption.md) із зазначеними опціями.

### Список параметрів

`options`

**Опції**

| Опция | Тип | Опис |
| --- | --- | --- |
| keyVaultClient | [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md) | Менеджер, який використовується для маршрутизації запитів ключів даних. Опція є обов'язковою (на відміну функції [MongoDB\\Driver\\Manager::createClientEncryption()](mongodb-driver-manager.createclientencryption.md) |
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

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md), якщо модуль був скомпільований без підтримки libmongocrypt.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.16.0 |  |
| Провайдер AWS KMS для шифрування на стороні клієнта тепер приймає параметр `"sessionToken"`, який можна вказувати для автентифікації з тимчасовими обліковими даними AWS. |  |

Добавлена поддержка поля`"tlsDisableOCSPEndpointCheck"` в опції `"tlsOptions"`

Якщо для KMS-провайдерів `"azure"`или`"gcp"` вказано порожній документ, драйвер спробує налаштувати провайдера, заповнивши [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

| | PECL mongodb 1.15.0 |

Якщо для KMS-провайдера `"aws"` вказано порожній документ, драйвер спробує налаштувати провайдера, заповнивши [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

### Дивіться також

-   [MongoDB\\Driver\\Manager::createClientEncryption()](mongodb-driver-manager.createclientencryption.md) \- Створення нового об'єкта ClientEncryption
-   [» Явне (ручне) шифрування рівня полів на стороні клієнта](https://www.mongodb.com/docs/manual/core/security-explicit-client-side-encryption/)у посібнику з MongoDB
