---
navigation:
  - mongodb-driver-clientencryption.encrypt.md: '« MongoDB\\Driver\\ClientEncryption::encrypt'
  - mongodb-driver-clientencryption.getkey.md: 'MongoDB\\Driver\\ClientEncryption::getKey »'
  - index.md: PHP Manual
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption
title: 'MongoDB\\Driver\\ClientEncryption::encryptExpression'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ClientEncryption::encryptExpression

(mongodb >=1.16.0)

MongoDB\\Driver\\ClientEncryption::encryptExpression — Шифрує збіг або агрегований вираз

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::encryptExpression(array|object $expr, ?array $options = null): object
```

Шифрує збіг або агрегований вираз запиту індексу діапазону.

Для виконання запиту із зашифрованим діапазоном корисного навантаження драйвер [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md) повинен бути налаштований з опцією `"autoEncryption"`Опция`"bypassQueryAnalysis"` автоматичного шифрування може мати значення \*\*`true`\*\*Опция`"bypassAutoEncryption"` автоматичного шифрування повинна мати значення **`false`**

> **Зауваження** :
> 
> Алгоритм роботи з діапазоном є експериментальним. Він призначений для громадського використання.
> 
> Драйвер PHP поки не підтримує запити діапазонів типів полів decimal128 BSON.

### Список параметрів

`expr`

Відповідність чи агрегований вираз, який необхідно зашифрувати. У виразах повинен використовуватися хоча б один із операторів `$gt` `$gte` `$lt`или`$lte`. Оператор верхнього рівня `$and` необхідний, навіть якщо використовується лише один оператор порівняння.

Приклад підтримуваного виразу відповідності (застосовується для запитів та етапу агрегації `$match`) виглядає наступним чином:

\[ '$and' => \[ \[ '' => \[ '$gt' => '' \] \] \[ '' => \[ '$lte' => '' \] \] \],\]

Приклад агрегованого виразу, що підтримується, виглядає наступним чином:

\[ '$and' => \[ \[ '$gte' => \[ '', '' \] \] \[ '$lt' => \[ '', '' \] \] \],\]

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

Повертає зашифрований вираз у вигляді об'єкта.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\EncryptionException](class.mongodb-driver-exception-encryptionexception.md)у разі виникнення помилки під час шифрування виразу.

### Дивіться також

-   [MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.md) \- Створює новий Manager MongoDB
