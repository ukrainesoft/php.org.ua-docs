---
navigation:
  - mongodb-driver-manager.construct.html: '« MongoDBDriverManager::construct'
  - mongodb-driver-manager.executebulkwrite.html: 'MongoDBDriverManager::executeBulkWrite »'
  - index.html: PHP Manual
  - class.mongodb-driver-manager.html: MongoDBDriverManager
title: 'MongoDBDriverManager::createClientEncryption'
---
# MongoDBDriverManager::createClientEncryption

(mongodb >=1.7.0)

MongoDBDriverManager::createClientEncryption — Створення нового об'єкта ClientEncryption

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::createClientEncryption(array $options): MongoDB\Driver\ClientEncryption
```

Створює новий об'єкт [MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html) із заданими параметрами.

### Список параметрів

`options`

**options**

| Параметр | Тип | Описание |
| --- | --- | --- |
| keyVaultClient | [MongoDBDriverManager](class.mongodb-driver-manager.html) | Менеджер використовується для маршрутизації запитів ключів даних до окремого кластера MongoDB. За промовчанням використовується поточний менеджер та кластер. |
| keyVaultNamespace | string | Повний простір імен (наприклад, `"databaseName.collectionName"`), що означає колекцію, яка містить усі ключі даних, що використовуються для шифрування та дешифрування. |
| kmsProviders | array |  |
| Документ, який містить конфігурацію для одного або кількох провайдерів KMS, які використовуються для шифрування ключів даних. Підтримуються провайдери `"aws"` `"azure"` `"gcp"` і `"local"`, і принаймні один з них повинен бути вказаний. |  |  |

Формат для `"aws"` виглядає наступним чином:

aws: { accessKeyId: , secretAccessKey:

Формат для `"azure"` виглядає наступним чином:

azure: { tenantId: , clientId: , clientSecret: , identityPlatformEndpoint: // За замовчуванням "login.microsoftonline.com"

Формат для `"gcp"` виглядає наступним чином:

gcp: { email: , privateKey: |, endpoint: // За замовчуванням "oauth2.googleapis.com"

Формат для `"kmip"` виглядає наступним чином:

kmip: { endpoint:

Формат для `"local"` виглядає наступним чином:

local: { // 96-байтовий головний ключ, який використовується для шифрування/дешифрування ключів даних key: | }

| | tlsOptions | array |

Документ, який містить конфігурацію TLS для одного або кількох KMS провайдерів. Підтримуються провайдери `"aws"` `"azure"` `"gcp"` і `"kmip"`. Усі провайдери підтримують такі опції:

: { tlsCaFile: , tlsCertificateKeyFile: , tlsCertificateKeyFilePassword:

### Значення, що повертаються

Повертає новий екземпляр [MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Викидає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) якщо модуль був скомпільований без підтримки libmongocrypt

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.12.0 |  |
| KMIP тепер підтримується як KMS провайдер для шифрування на стороні клієнта і може бути налаштований за допомогою параметра `"kmsProviders"` |  |

Доданий параметр `"tlsOptions"`

| | PECL mongodb 1.10.0 Azure та GCP тепер підтримуються як постачальники KMS для шифрування на стороні клієнта і можуть бути налаштовані в полі `"kmsProviders"` параметра драйвера `"autoEncryption"`. Рядки в кодуванні Base64 тепер приймаються як альтернатива [MongoDBBSONBinary](class.mongodb-bson-binary.html) для параметрів усередині `"kmsProviders"`.

### Дивіться також

-   [MongoDBDriverClientEncryption::construct()](mongodb-driver-clientencryption.construct.html) - Створює новий об'єкт ClientEncryption
-   Сторінка в посібнику з MongoDB: [» Явное (ручное) шифрование на уровне поля на стороне клиента](https://www.mongodb.com/docs/manual/core/security-explicit-client-side-encryption/)
