---
navigation:
  - class.mongodb-driver-exception-bulkwriteexception.md: « MongoDB\\Driver\\Exception\\BulkWriteException
  - mongodb-driver-commandexception.getresultdocument.md: 'MongoDB\\Driver\\Exception\\CommandException::getResultDocument »'
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\CommandException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\CommandException

(mongodb >= 1.5.0)

## Вступ

Викидається у разі виникнення помилки команди.

## Огляд класів

```classsynopsis



    
     
      abstract
      class MongoDB\Driver\Exception\CommandException
     

     
      extends
       MongoDB\Driver\Exception\ServerException
     

     implements 
       MongoDB\Driver\Exception\Exception {

    /* Свойства */
    
     protected
     object
      $resultDocument;


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


    /* Методы */
    
   final public getResultDocument(): object


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

## Властивості

resultDocument

Документ результату, пов'язаний із невдалою командою.

## Зміст

-   [MongoDB\\Driver\\Exception\\CommandException::getResultDocument](mongodb-driver-commandexception.getresultdocument.md)— Повертає результат документа для невдалої команди
