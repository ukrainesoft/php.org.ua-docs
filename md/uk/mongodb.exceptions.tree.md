MongoDB Exception Class Tree

-   [« MongoDBDriverExceptionWriteException::getWriteResult](mongodb-driver-writeexception.getwriteresult.html)
    
-   [MySQL »](set.mysqlinfo.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverException](mongodb.exceptions.html)
    
-   MongoDB Exception Class Tree
    

# MongoDB Exception Class Tree

Class hierarchy для MongoDB виразів є моделювання після того, що [SPL Exceptions](spl.exceptions.html). Base classes extend their SPL counterpart and all exception classes in the extension implemente the [MongoDBDriverExceptionException](class.mongodb-driver-exception-exception.html) interface.

-   [MongoDBDriverExceptionLogicException](class.mongodb-driver-exception-logicexception.html) (extends [LogicException](class.logicexception.html)
-   [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) (extends [InvalidArgumentException](class.invalidargumentexception.html)
-   [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) (extends [UnexpectedValueException](class.unexpectedvalueexception.html)
-   [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) (extends [RuntimeException](class.runtimeexception.html)
    -   [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.html)
        -   [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
        -   [MongoDBDriverExceptionConnectionTimeoutException](class.mongodb-driver-exception-connectiontimeoutexception.html)
        -   [MongoDBDriverExceptionSSLConnectionException](class.mongodb-driver-exception-sslconnectionexception.html) (Deprecated)
    -   [MongoDBDriverExceptionEncryptionException](class.mongodb-driver-exception-encryptionexception.html)
    -   [MongoDBDriverExceptionServerException](class.mongodb-driver-exception-serverexception.html)
        -   [MongoDBDriverExceptionCommandException](class.mongodb-driver-exception-commandexception.html)
        -   [MongoDBDriverExceptionExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.html)
        -   [MongoDBDriverExceptionWriteException](class.mongodb-driver-exception-writeexception.html)
            -   [MongoDBDriverExceptionBulkWriteException](class.mongodb-driver-exception-bulkwriteexception.html)