---
navigation:
  - mongodb-driver-clientencryption.deletekey.md: '« MongoDB\\Driver\\ClientEncryption::deleteKey'
  - mongodb-driver-clientencryption.encryptexpression.md: 'MongoDB\\Driver\\ClientEncryption::encryptExpression »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::encrypt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::encrypt

(mongodb >=1.7.0)

MongoDB\\Driver\\ClientEncryption::encrypt — Шифрує дані

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::encrypt(mixed $value, ?array $options = null): MongoDB\BSON\Binary
```

Шифрує дані.

### Список параметрів

`value`

Значення для шифрування. Метод може зашифрувати будь-які дані, які можуть бути записані MongoDB.

`options`

**Encryption options**

| Опция | Тип | Опис |
| --- | --- | --- |
| algorithm | string |  |
| Алгоритм шифрування, який використовуватиметься. Опція є обов'язковою. Вкажіть одну з наступних [констант ClientEncryption](class.mongodb-driver-clientencryption.md#mongodb-driver-clientencryption.constants) : |  |  |

-   **`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_DETERMINISTIC`**
-   **`MongoDB\Driver\ClientEncryption::AEAD_AES_256_CBC_HMAC_SHA_512_RANDOM`**
-   **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**
-   **`MongoDB\Driver\ClientEncryption::ALGORITHM_UNINDEXED`**
-   **`MongoDB\Driver\ClientEncryption::ALGORITHM_RANGE_PREVIEW`**

| | contentionFactor | int |

Коефіцієнт стримування в оцінці запитів з індексованими, зашифрованими корисними навантаженнями.

Опція застосовується та може бути вказана лише тоді, коли опція `algorithm` дорівнює **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**или**`MongoDB\Driver\ClientEncryption::ALGORITHM_RANGE_PREVIEW`**

| | keyAltName | string |

Ідентифікує документ колекції сховища ключів за `keyAltName`. Опція є взаємовиключною з `keyId` і потрібно рівно один.

| | keyId |[MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md)

Ідентифікує ключ даних щодо `_id`. Значення UUID (двійковий підтип 4). Опція є взаємовиключною з `keyAltName` і потрібно рівно один.

| | queryType | string |

Тип запиту для оцінки запитів із індексованими, зашифрованими корисними навантаженнями. Вкажіть одну з наступних [констант ClientEncryption](class.mongodb-driver-clientencryption.md#mongodb-driver-clientencryption.constants) :

-   **`MongoDB\Driver\ClientEncryption::QUERY_TYPE_EQUALITY`**
-   **`MongoDB\Driver\ClientEncryption::QUERY_TYPE_RANGE_PREVIEW`**

Опція застосовується та може бути вказана лише тоді, коли опція `algorithm` дорівнює **`MongoDB\Driver\ClientEncryption::ALGORITHM_INDEXED`**или**`MongoDB\Driver\ClientEncryption::ALGORITHM_RANGE_PREVIEW`**

| | rangeOpts | array |

Опції індексу для поля, що шифрується, з підтримкою запитів "rangePreview". Наведені нижче параметри повинні відповідати значенням, встановленим у `encryptedFields` цільової колекції. Для полів типу double та decimal128 BSON, `min` `max`и`precision` повинні бути або всі встановлені, або всі повинні бути відсутніми.

**Опції індексу діапазону**

| Опция | Тип | Опис |
| --- | --- | --- |
| min | [mixed](language.types.declarations.md#language.types.declarations.mixed) | Обов'язкове, якщо встановлено значення `precision` |
| max | [mixed](language.types.declarations.md#language.types.declarations.mixed) | Обов'язкове, якщо встановлено значення `precision` |
| sparsity | int | Обов'язкове. |
| precision | int | Необов'язкове. Може бути встановлений лише для типів полів BSON double або decimal128. |

### Значення, що повертаються

Повертає зашифровані дані у вигляді об'єкту [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md) з підтипом 6.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\EncryptionException](class.mongodb-driver-exception-encryptionexception.md)якщо при шифруванні виникла помилка

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.14.0 | Додані опції `"contentionFactor"`и`"queryType"` |

### Дивіться також

-   [MongoDB\\Driver\\ClientEncryption::decrypt()](mongodb-driver-clientencryption.decrypt.md) \- Розшифрувати дані
