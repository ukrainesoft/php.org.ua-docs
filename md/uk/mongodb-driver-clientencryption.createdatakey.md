---
navigation:
  - mongodb-driver-clientencryption.construct.md: '« MongoDB\\Driver\\ClientEncryption::\_\_construct'
  - mongodb-driver-clientencryption.decrypt.md: 'MongoDB\\Driver\\ClientEncryption::decrypt »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::createDataKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::createDataKey

(mongodb >=1.7.0)

MongoDB\\Driver\\ClientEncryption::createDataKey — Створює документ із ключем

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::createDataKey(string $kmsProvider, ?array $options = null): MongoDB\BSON\Binary
```

Створює новий документ із ключем шифрування та кладе його в колекцію сховища ключів.

### Список параметрів

`kmsProvider`

Провайдер KMS (`"local"` `"aws"`), який використовуватиметься для шифрування нового ключа даних.

`options`

**Опції**

| Опция | Тип | Опис |
| --- | --- | --- |
| masterKey | array |  |
| Документ masterKey визначає специфічний для KMS ключ, який використовується для шифрування нового ключа даних. Параметр обов'язковий, якщо параметр `kmsProvider` не є `"local"` |  |  |

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

| | keyAltNames | array |

Опціональний список альтернативних імен, які використовуються для посилання на ключ. Якщо ключ створено з використанням альтернативних імен, то при шифруванні можна посилатися на унікальне альтернативне ім'я замість `_id`

| | keyMaterial |[MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md)

Необов'язкове 96-байтове значення для використання як матеріал користувача ключа для створюваного ключа даних. Якщо задано keyMaterial, то використовується матеріал користувача ключа для шифрування і розшифровки даних. В іншому випадку матеріал ключа для нового ключа даних генерується криптографічно захищеного випадкового пристрою.

### Значення, що повертаються

Повертає ідентифікатор нового ключа як об'єкт [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md) із підтипом 4 (UUID).

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)у разі інших помилок.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Добавлена опция`"keyMaterial"` |
| PECL mongodb 1.10.0 | Як постачальники KMS для шифрування на стороні клієнта тепер підтримуються Azure та GCP. |
