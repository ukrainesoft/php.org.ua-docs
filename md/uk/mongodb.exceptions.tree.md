---
navigation:
  - mongodb-driver-writeexception.getwriteresult.html: '« MongoDBDriverExceptionWriteException::getWriteResult'
  - set.mysqlinfo.html: MySQL »
  - index.html: PHP Manual
  - mongodb.exceptions.html: MongoDBDriverException
title: MongoDB Exception Class Tree
---
# MongoDB Exception Class Tree

Class hierarchy для MongoDB виразів є моделювання після того, що [SPL Exceptions](spl.exceptions.html). Base classes extend their SPL counterpart and all exception classes in the extension implemente the [MongoDBDriverExceptionException](class.mongodb-driver-exception-exception.md) interface.

-   [MongoDBDriverExceptionLogicException](class.mongodb-driver-exception-logicexception.html) (extends [LogicException](class.logicexception.md)
-   [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) (extends [InvalidArgumentException](class.invalidargumentexception.md)
-   [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) (extends [UnexpectedValueException](class.unexpectedvalueexception.md)
-   [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) (extends [RuntimeException](class.runtimeexception.md)
    -   [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
        -   [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
        -   [MongoDBDriverExceptionConnectionTimeoutException](class.mongodb-driver-exception-connectiontimeoutexception.md)
        -   [MongoDBDriverExceptionSSLConnectionException](class.mongodb-driver-exception-sslconnectionexception.md) (Deprecated)
    -   [MongoDBDriverExceptionEncryptionException](class.mongodb-driver-exception-encryptionexception.md)
    -   [MongoDBDriverExceptionServerException](class.mongodb-driver-exception-serverexception.md)
        -   [MongoDBDriverExceptionCommandException](class.mongodb-driver-exception-commandexception.md)
        -   [MongoDBDriverExceptionExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.md)
        -   [MongoDBDriverExceptionWriteException](class.mongodb-driver-exception-writeexception.md)
            -   [MongoDBDriverExceptionBulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md)
