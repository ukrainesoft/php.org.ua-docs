Створює новий об'єкт ClientEncryption

-   [« MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html)
    
-   [MongoDBDriverClientEncryption::createDataKey »](mongodb-driver-clientencryption.createdatakey.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html)
    
-   Створює новий об'єкт ClientEncryption
    

# MongoDBDriverClientEncryption::construct

(mongodb >=1.14.0)

MongoDBDriverClientEncryption::construct — Створює новий об'єкт ClientEncryption

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::__construct(array $options)
```

Створює новий об'єкт [MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html) із зазначеними опціями.

### Список параметрів

`options`

**Опції**

| Опция | Тип | Описание |
| --- | --- | --- |
| keyVaultClient | [MongoDBDriverManager](class.mongodb-driver-manager.html) | Менеджер, який використовується для маршрутизації запитів ключів даних. Опція є обов'язковою (на відміну функції [MongoDBDriverManager::createClientEncryption()](mongodb-driver-manager.createclientencryption.html) |
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

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Викидає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html)якщо модуль був скомпільований без підтримки libmongocrypt.

### Дивіться також

-   [MongoDBDriverManager::createClientEncryption()](mongodb-driver-manager.createclientencryption.html) - Створення нового об'єкта ClientEncryption
-   [» Явное (ручное) шифрование уровня полей на стороне клиента](https://www.mongodb.com/docs/manual/core/security-explicit-client-side-encryption/) у посібнику з MongoDB