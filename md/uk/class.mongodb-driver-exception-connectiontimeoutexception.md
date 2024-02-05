---
navigation:
  - class.mongodb-driver-exception-connectionexception.md: « MongoDB\\Driver\\Exception\\ConnectionException
  - class.mongodb-driver-exception-encryptionexception.md: MongoDB\\Driver\\Exception\\EncryptionException »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\ConnectionTimeoutException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\ConnectionTimeoutException

(mongodb >= 1.0.0)

## Вступ

Викидається, коли драйверу не вдається встановити з'єднання з базою даних протягом певного періоду часу ([connectTimeoutMS](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-urioptions)). або вибір сервера не вдався ([serverSelectionTimeoutMS](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-urioptions)

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Exception\ConnectionTimeoutException
     

     
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
