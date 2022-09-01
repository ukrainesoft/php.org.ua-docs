---
navigation:
  - class.mongodb-driver-exception-exception.html: « MongoDBDriverExceptionException
  - class.mongodb-driver-exception-invalidargumentexception.html: MongoDBDriverExceptionInvalidArgumentException »
  - index.html: PHP Manual
  - mongodb.exceptions.html: MongoDBDriverException
title: Клас MongoDBDriverExceptionExecutionTimeoutException
---
# Клас MongoDBDriverExceptionExecutionTimeoutException

(mongodb >= 1.0.0)

## Вступ

Викидається, коли запит або команда не завершується протягом певного періоду часу (наприклад, [» maxTimeMS](https://www.mongodb.com/docs/manual/tutorial/terminate-running-operations/#maxtimems)

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Exception\ExecutionTimeoutException
     

     
      extends
       MongoDB\Driver\Exception\ServerException
     

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

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.5.0 |  |
| Тепер цей клас розширює [MongoDBDriverExceptionServerException](class.mongodb-driver-exception-serverexception.html) замість [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) |  |
