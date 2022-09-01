---
navigation:
  - class.mongodb-driver-exception-connectiontimeoutexception.html: « MongoDBDriverExceptionConnectionTimeoutException
  - class.mongodb-driver-exception-exception.html: MongoDBDriverExceptionException »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDBDriverException
title: Клас MongoDBDriverExceptionEncryptionException
---
# Клас MongoDBDriverExceptionEncryptionException

(mongodb >= 1.7.0)

## Вступ

Базовий клас для виключень кидаються у процесі шифрування за клієнта.

## Огляд класів

```classsynopsis


    
    
     
      class MongoDB\Driver\Exception\EncryptionException
     

     
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
