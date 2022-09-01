---
navigation:
  - mongodb.exceptions.html: « MongoDBDriverException
  - class.mongodb-driver-exception-bulkwriteexception.html: MongoDBDriverExceptionBulkWriteException »
  - index.html: PHP Manual
  - mongodb.exceptions.html: MongoDBDriverException
title: Клас MongoDBDriverExceptionAuthenticationException
---
# Клас MongoDBDriverExceptionAuthenticationException

(mongodb >= 1.0.0)

## Вступ

Викидається, коли драйвер не може виконати автентифікацію із сервером.

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\AuthenticationException
     

     
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
