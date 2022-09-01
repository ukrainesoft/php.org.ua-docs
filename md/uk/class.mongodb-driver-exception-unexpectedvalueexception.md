---
navigation:
  - class.mongodb-driver-exception-sslconnectionexception.html: « MongoDBDriverExceptionSSLConnectionException
  - class.mongodb-driver-exception-writeexception.html: MongoDBDriverExceptionWriteException »
  - index.html: PHP Manual
  - mongodb.exceptions.html: MongoDBDriverException
title: Клас MongoDBDriverExceptionUnexpectedValueException
---
# Клас MongoDBDriverExceptionUnexpectedValueException

(mongodb >= 1.0.0)

## Вступ

Викидається, коли драйвер стикається з несподіваним значенням (наприклад, під час серіалізації або десеріалізації BSON).

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\UnexpectedValueException
     

     
      extends
       UnexpectedValueException
     

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
