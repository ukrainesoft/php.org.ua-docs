MongoDB Exception Class Tree

-   [« MongoDB\\Driver\\Exception\\WriteException::getWriteResult](mongodb-driver-writeexception.getwriteresult.html)
    
-   [MySQL »](set.mysqlinfo.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Exception](mongodb.exceptions.html)
    
-   MongoDB Exception Class Tree
    

# MongoDB Exception Class Tree

Class hierarchy для MongoDB виразів є моделювання після того, що [SPL Exceptions](spl.exceptions.html). Base classes extend their SPL counterpart and all exception classes in the extension implemente the [MongoDB\\Driver\\Exception\\Exception](class.mongodb-driver-exception-exception.html) interface.

-   [MongoDB\\Driver\\Exception\\LogicException](class.mongodb-driver-exception-logicexception.html) (extends [LogicException](class.logicexception.html)
-   [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) (extends [InvalidArgumentException](class.invalidargumentexception.html)
-   [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) (extends [UnexpectedValueException](class.unexpectedvalueexception.html)
-   [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) (extends [RuntimeException](class.runtimeexception.html)
    -   [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html)
        -   [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
        -   [MongoDB\\Driver\\Exception\\ConnectionTimeoutException](class.mongodb-driver-exception-connectiontimeoutexception.html)
        -   [MongoDB\\Driver\\Exception\\SSLConnectionException](class.mongodb-driver-exception-sslconnectionexception.html) (Deprecated)
    -   [MongoDB\\Driver\\Exception\\EncryptionException](class.mongodb-driver-exception-encryptionexception.html)
    -   [MongoDB\\Driver\\Exception\\ServerException](class.mongodb-driver-exception-serverexception.html)
        -   [MongoDB\\Driver\\Exception\\CommandException](class.mongodb-driver-exception-commandexception.html)
        -   [MongoDB\\Driver\\Exception\\ExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.html)
        -   [MongoDB\\Driver\\Exception\\WriteException](class.mongodb-driver-exception-writeexception.html)
            -   [MongoDB\\Driver\\Exception\\BulkWriteException](class.mongodb-driver-exception-bulkwriteexception.html)