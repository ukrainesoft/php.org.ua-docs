---
navigation:
  - class.mongodb-driver-exception-authenticationexception.md: « MongoDB\\Driver\\Exception\\AuthenticationException
  - class.mongodb-driver-exception-commandexception.md: MongoDB\\Driver\\Exception\\CommandException »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\BulkWriteException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\BulkWriteException

(mongodb >= 1.0.0)

## Вступ

Викидається у разі невдалої масової операції запису.

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\BulkWriteException
     

     
      extends
       MongoDB\Driver\Exception\WriteException
     

     implements 
       MongoDB\Driver\Exception\Exception {

    /* Наследуемые свойства */
    
     protected
     MongoDB\Driver\WriteResult
      $writeResult;

    
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
    
   final public MongoDB\Driver\Exception\WriteException::getWriteResult(): MongoDB\Driver\WriteResult

    
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
