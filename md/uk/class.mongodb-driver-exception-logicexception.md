---
navigation:
  - class.mongodb-driver-exception-invalidargumentexception.html: « MongoDBDriverExceptionInvalidArgumentException
  - class.mongodb-driver-exception-runtimeexception.html: MongoDBDriverExceptionRuntimeException »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDBDriverException
title: Клас MongoDBDriverExceptionLogicException
---
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
