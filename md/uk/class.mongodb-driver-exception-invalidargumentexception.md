---
navigation:
  - class.mongodb-driver-exception-executiontimeoutexception.md: « MongoDB\\Driver\\Exception\\ExecutionTimeoutException
  - class.mongodb-driver-exception-logicexception.md: MongoDB\\Driver\\Exception\\LogicException »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\InvalidArgumentException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\InvalidArgumentException

(mongodb >= 1.0.0)

## Вступ

Викидається, коли метод драйвера передано некоректні аргументи (наприклад, неприпустимі типи опцій).

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\InvalidArgumentException
     

     
      extends
       InvalidArgumentException
     

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
