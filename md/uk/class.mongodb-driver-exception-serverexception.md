---
navigation:
  - mongodb-driver-runtimeexception.haserrorlabel.md: '« MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel'
  - class.mongodb-driver-exception-sslconnectionexception.md: MongoDB\\Driver\\Exception\\SSLConnectionException »
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\ServerException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\ServerException

(mongodb >= 1.5.0)

## Вступ

Базовий клас для винятків, викинутих сервером. Код цього виключення та його підкласи будуть відповідати вихідному коду помилки із сервера.

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\ServerException
     

     
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
