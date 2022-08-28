Шифрує дані

-   [« MongoDB\\Driver\\ClientEncryption::decrypt](mongodb-driver-clientencryption.decrypt.html)
    
-   [MongoDB\\Driver\\ServerApi »](class.mongodb-driver-serverapi.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ClientEncryption](class.mongodb-driver-clientencryption.html)
    
-   Шифрує дані
    

# MongoDBDriverClientEncryption::encrypt

(mongodb >=1.7.0)

MongoDBDriverClientEncryption::encrypt — Шифрує дані

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::encrypt(mixed $value, ?array $options = null): MongoDB\BSON\Binary
```

Шифрує дані.

### Список параметрів

`value`

Значення для шифрування. Метод може зашифрувати будь-які дані, які можуть бути записані MongoDB.

`options`

**Опції шифрування**

| Опция                                                                                                                                                                                                             | Тип    | Описание |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|----------|
| algorithm                                                                                                                                                                                                         | string |          |
| Алгоритм шифрування, який використовуватиметься. Опція є обов'язковою. Вкажіть одну з наступних [констант ClientEncryption](class.mongodb-driver-clientencryption.html#mongodb-driver-clientencryption.constants) |        |          |

-   **`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_DETERMINISTIC`**
-   **`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_RANDOM`**
-   **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**
-   **`MongoDB\Driver\ClientEncryption::ALGORITHM_UNINDEXED`**

| | contentionFactor | int |

Коефіцієнт стримування в оцінці запитів з індексованими, зашифрованими корисними навантаженнями.

Опція застосовується та може бути вказана лише тоді, коли опція `algorithm` дорівнює **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**

> **Зауваження**: Queryable Encryption знаходиться в стадії публічного перегляду і доступний для ознайомлювальних цілей. Його поки що не рекомендується використовувати для розгортань у продакшені, оскільки можуть бути внесені зміни. Додаткову інформацію дивіться у блозі [» Queryable Encryption Preview](https://www.mongodb.com/blog/post/mongodb-releases-queryable-encryption-preview/)

| | keyAltName | string |

Задає документ колекції сховища ключів `keyAltName`. Взаємовиключна з опцією `keyId`, потрібна лише одна з них.

| | keyId | [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)

Задає ключ даних по `_id`. Значення типу UUID (бінарний підтип 4). Взаємовиключна з опцією `keyAltName`, потрібна лише одна з них.

| | QueryType | int |

Тип запиту для оцінки запитів з індексованим, зашифрованим корисним навантаженням. Вкажіть одну з наступних [констант ClientEncryption](class.mongodb-driver-clientencryption.html#mongodb-driver-clientencryption.constants)

-   **`MongoDB\Driver\ClientEncryption::QUERY_TYPE_EQUALITY`**

Опція застосовується та може бути вказана лише тоді, коли опція `algorithm` дорівнює **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**

> **Зауваження**: Queryable Encryption знаходиться в стадії публічного перегляду і доступний для ознайомлювальних цілей. Його поки що не рекомендується використовувати для розгортань у продакшені, оскільки можуть бути внесені зміни. Додаткову інформацію дивіться у блозі [» Queryable Encryption Preview](https://www.mongodb.com/blog/post/mongodb-releases-queryable-encryption-preview/)

### Значення, що повертаються

Повертає зашифровані дані у вигляді об'єкту [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html) з підтипом 6.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Викидає виняток [MongoDB\\Driver\\Exception\\EncryptionException](class.mongodb-driver-exception-encryptionexception.html) якщо при шифруванні виникла помилка

### список змін

| Версия              | Описание                                          |
|---------------------|---------------------------------------------------|
| PECL mongodb 1.14.0 | Додані опції `"contentionFactor"` і `"queryType"` |

### Дивіться також

-   [MongoDB\\Driver\\ClientEncryption::decrypt()](mongodb-driver-clientencryption.decrypt.html) - Розшифрувати дані