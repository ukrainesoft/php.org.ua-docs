---
navigation:
  - mongodb-driver-writeexception.getwriteresult.md: '« MongoDBDriverExceptionWriteException::getWriteResult'
  - set.mysqlinfo.md: MySQL »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDBDriverException
title: MongoDB Exception Class Tree
---
# MongoDB Exception Class Tree

Class hierarchy для MongoDB виразів є моделювання після того, що [SPL Exceptions](spl.exceptions.md). Base classes extend their SPL counterpart and all exception classes in the extension implemente the [MongoDBDriverExceptionException](class.mongodb-driver-exception-exception.md) interface.

-   [MongoDBDriverExceptionLogicException](class.mongodb-driver-exception-logicexception.md) (extends [LogicException](class.logicexception.md)
-   [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) (extends [InvalidArgumentException](class.invalidargumentexception.md)
-   [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md) (extends [UnexpectedValueException](class.unexpectedvalueexception.md)
-   [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md) (extends [RuntimeException](class.runtimeexception.md)
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
