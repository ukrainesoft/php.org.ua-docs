---
navigation:
  - mongodb-driver-commandexception.getresultdocument.md: '« MongoDB\\Driver\\Exception\\CommandException::getResultDocument'
  - class.mongodb-driver-exception-connectiontimeoutexception.md: MongoDB\\Driver\\Exception\\ConnectionTimeoutException »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\ConnectionException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\ConnectionException

(mongodb >= 1.0.0)

## Вступ

Базовий клас для виключень, коли драйвер не може встановити підключення до бази даних.

## Огляд класів

```classsynopsis


    
    
     
      class MongoDB\Driver\Exception\ConnectionException
     

     
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
