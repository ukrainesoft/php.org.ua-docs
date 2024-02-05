---
navigation:
  - class.mongodb-driver-exception-unexpectedvalueexception.md: « MongoDB\\Driver\\Exception\\UnexpectedValueException
  - mongodb-driver-writeexception.getwriteresult.md: 'MongoDB\\Driver\\Exception\\WriteException::getWriteResult »'
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\WriteException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\WriteException

(mongodb >= 1.0.0)

## Вступ

Базовий клас для винятків, спричинених невдалою операцією запису. Цей виняток містить об'єкт [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)

## Огляд класів

```classsynopsis


    
    
     
      abstract
      class MongoDB\Driver\Exception\WriteException
     

     
      extends
       MongoDB\Driver\Exception\ServerException
     

     implements 
       MongoDB\Driver\Exception\Exception {
    
    /* Свойства */
    
     protected
     MongoDB\Driver\WriteResult
      $writeResult;


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
    
   final public getWriteResult(): MongoDB\Driver\WriteResult


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

writeResult

Об'єкт [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md), пов'язаний із невдалою операцією запису.

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.5.0 |  |
| Тепер клас успадковується від [MongoDB\\Driver\\Exception\\ServerException](class.mongodb-driver-exception-serverexception.md) замість [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md) |  |

## Зміст

-   [MongoDB\\Driver\\Exception\\WriteException::getWriteResult](mongodb-driver-writeexception.getwriteresult.md)— Повертає WriteResult для операції запису помилкою, що закінчилася.
