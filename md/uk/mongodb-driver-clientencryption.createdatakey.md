Створює ключ шифрування

-   [« MongoDBDriverClientEncryption::construct](mongodb-driver-clientencryption.construct.html)
    
-   [MongoDBDriverClientEncryption::decrypt »](mongodb-driver-clientencryption.decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html)
    
-   Створює ключ шифрування
    

# MongoDBDriverClientEncryption::createDataKey

(mongodb >=1.7.0)

MongoDBDriverClientEncryption::createDataKey — Створює ключ шифрування

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::createDataKey(string $kmsProvider, ?array $options = null): MongoDB\BSON\Binary
```

Створює новий документ із ключем шифрування та кладе його в колекцію сховища ключів.

### Список параметрів

`kmsProvider`

Провайдер KMS (`"local"` `"aws"` `"azure"` `"gcp"`), який використовуватиметься для шифрування нового ключа.

`options`

**Опції**

| Опция                                                                                                                                                        | Тип   | Описание |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|----------|
| masterKey                                                                                                                                                    | array |          |
| masterKey задає відповідний для KMS ключ, який використовуватиметься для шифрування нового ключа. Ця опція є обов'язковою, якщо `kmsProvider` не є `"local"` |       |          |

Якщо в `kmsProvider` вказано значення `"aws"`, цей параметр є обов'язковим і має такі поля:

**Опції masterKey для AWS**

| Опция    | Тип    | Описание                                                                                                  |
|----------|--------|-----------------------------------------------------------------------------------------------------------|
| region   | string | Обов'язковий                                                                                              |
| key      | string | Обов'язковий. Amazon Resource Name (ARN) для майстер ключа користувача (CMK) AWS                          |
| endpoint | string | Необов'язковий. Альтернативний ідентифікатор хоста для надсилання запитів KMS. Може включати номер порту. |

Якщо в `kmsProvider` вказано значення `"azure"`, цей параметр є обов'язковим і має такі поля:

**Опції masterKey для Azure**

| Опция            | Тип    | Описание                                                                                      |
|------------------|--------|-----------------------------------------------------------------------------------------------|
| keyVaultEndpoint | string | Обов'язкове. Хост із необов'язковим портом (наприклад, example.vault.azure.net).              |
| keyName          | string | Обов'язкове.                                                                                  |
| keyVersion       | string | Необов'язкове. Конкретна версія ключа За промовчанням використовується первинна версія ключа. |

Якщо в `kmsProvider` вказано значення `"gcp"`, цей параметр є обов'язковим і має такі поля:

**Опції masterKey для GCP**

| Опция      | Тип    | Описание                                                                                      |
|------------|--------|-----------------------------------------------------------------------------------------------|
| projectId  | string | Обов'язкове.                                                                                  |
| location   | string | Обов'язкове.                                                                                  |
| keyRing    | string | Обов'язкове.                                                                                  |
| keyName    | string | Обов'язкове.                                                                                  |
| keyVersion | string | Необов'язкове. Конкретна версія ключа За промовчанням використовується первинна версія ключа. |
| endpoint   | string | Необов'язкове. Хост з необов'язковим портом. За промовчанням cloudkms.googleapis.com.         |

| | keyAltNames | array |

Опціональний список альтернативних імен, які використовуються для посилання на ключ. Якщо ключ створено з використанням альтернативних імен, то при шифруванні можна посилатися на унікальне альтернативне ім'я замість `_id`

### Значення, що повертаються

Повертає ідентифікатор нового ключа як об'єкт [MongoDBBSONBinary](class.mongodb-bson-binary.html) із підтипом 4 (UUID).

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Кидає виняток [MongoDBDriverExceptionEncryptionException](class.mongodb-driver-exception-encryptionexception.html) якщо в процесі створення ключа сталася помилка

### список змін

| Версия              | Описание                                                                                 |
|---------------------|------------------------------------------------------------------------------------------|
| PECL mongodb 1.10.0 | Як постачальники KMS для шифрування на стороні клієнта тепер підтримуються Azure та GCP. |