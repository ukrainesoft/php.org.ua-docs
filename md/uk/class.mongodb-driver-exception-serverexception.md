Клас MongoDBDriverExceptionServerException

-   [« MongoDBDriverExceptionRuntimeException::hasErrorLabel](mongodb-driver-runtimeexception.haserrorlabel.html)
    
-   [MongoDBDriverExceptionSSLConnectionException »](class.mongodb-driver-exception-sslconnectionexception.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverException](mongodb.exceptions.html)
    
-   Клас MongoDBDriverExceptionServerException
    

# Клас MongoDBDriverExceptionServerException

(mongodb >= 1.5.0)

## Вступ

Базовий клас для винятків, викинутих сервером. Код цього виключення та його підкласи будуть відповідати вихідному коду помилки із сервера.

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\ServerException
     

     
      extends
       MongoDB\Driver\Exception\RuntimeException
     

     implements 
       MongoDB\Driver\Exception\Exception {

    /* Наследуемые свойства */
    
     protected
     ?array
      $errorLabels;

    
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
    
   final public MongoDB\Driver\Exception\RuntimeException::hasErrorLabel(string $errorLabel): bool

    
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