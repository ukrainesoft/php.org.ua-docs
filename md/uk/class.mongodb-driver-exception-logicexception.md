Клас MongoDBDriverExceptionLogicException

-   [« MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
    
-   [MongoDBDriverExceptionRuntimeException »](class.mongodb-driver-exception-runtimeexception.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverException](mongodb.exceptions.md)
    
-   Клас MongoDBDriverExceptionLogicException
    

# Клас MongoDBDriverExceptionLogicException

(mongodb >= 1.0.0)

## Вступ

Викидається при неправильному використанні драйвера (наприклад, перемотування на початок курсору).

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\LogicException
     

     
      extends
       LogicException
     

     implements 
       MongoDB\Driver\Exception\Exception {

    /* Наследуемые свойства */
    
    
     protected
     string
      $message = "";
private
     string
      $string = "";
protected
     int
      $code;
protected
     string
      $file = "";
protected
     int
      $line;
private
     array
      $trace = [];
private
     ?Throwable
      $previous = null;


    /* Наследуемые методы */
    
    
   final public Exception::getMessage(): string
final public Exception::getPrevious(): ?Throwable
final public Exception::getCode(): int
final public Exception::getFile(): string
final public Exception::getLine(): int
final public Exception::getTrace(): array
final public Exception::getTraceAsString(): string
public Exception::__toString(): string
private Exception::__clone(): void


   }
```