Клас MongoDBDriverExceptionSSLConnectionException (застарілий)

-   [« MongoDBDriverExceptionServerException](class.mongodb-driver-exception-serverexception.html)
    
-   [MongoDBDriverExceptionUnexpectedValueException »](class.mongodb-driver-exception-unexpectedvalueexception.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverException](mongodb.exceptions.html)
    
-   Клас MongoDBDriverExceptionSSLConnectionException (застарілий)
    

# Клас MongoDBDriverExceptionSSLConnectionException (застарілий)

(mongodb >= 1.0.0)

**Увага**

Цей клас винятків застарів і може бути вилучений у майбутній основній версії. Драйвер ніколи не викине цей виняток.

## Вступ

Викидається, коли драйверу не вдається встановити з'єднання SSL з сервером.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Exception\SSLConnectionException
     

     
      extends
       MongoDB\Driver\Exception\ConnectionException
     

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