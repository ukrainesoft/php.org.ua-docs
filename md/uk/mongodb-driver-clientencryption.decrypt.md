Розшифрувати дані

-   [« MongoDBDriverClientEncryption::createDataKey](mongodb-driver-clientencryption.createdatakey.html)
    
-   [MongoDBDriverClientEncryption::encrypt »](mongodb-driver-clientencryption.encrypt.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html)
    
-   Розшифрувати дані
    

# MongoDBDriverClientEncryption::decrypt

(mongodb >=1.7.0)

MongoDBDriverClientEncryption::decrypt — Розшифрувати дані

### Опис

```methodsynopsis
final public MongoDB\Driver\ClientEncryption::decrypt(MongoDB\BSON\Binary $value): mixed
```

Розшифровує значення.

### Список параметрів

`value`

Об'єкт класу [MongoDBBSONBinary](class.mongodb-bson-binary.html) з підтипом 6, що містить зашифровані дані.

### Значення, що повертаються

Повертає розшифровані дані у тому вигляді, як вони були передані в [MongoDBDriverClientEncryption::encrypt()](mongodb-driver-clientencryption.encrypt.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Кидає виняток [MongoDBDriverExceptionEncryptionException](class.mongodb-driver-exception-encryptionexception.html) якщо в процесі дешифрування сталася помилка

### Дивіться також

-   [MongoDBDriverClientEncryption::encrypt()](mongodb-driver-clientencryption.encrypt.html) - Шифрує дані