Клас MongoDBDriverExceptionWriteException

-   [« MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)
    
-   [MongoDB\\Driver\\Exception\\WriteException::getWriteResult »](mongodb-driver-writeexception.getwriteresult.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Exception](mongodb.exceptions.html)
    
-   Клас MongoDBDriverExceptionWriteException
    

# Клас MongoDBDriverExceptionWriteException

(mongodb >= 1.0.0)

## Вступ

Базовий клас для винятків, спричинених невдалою операцією запису. Цей виняток містить об'єкт [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html)

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

Об'єкт [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html), пов'язаний із невдалою операцією запису.

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.5.0 |  |
| Тепер клас успадковується від [MongoDB\\Driver\\Exception\\ServerException](class.mongodb-driver-exception-serverexception.html) замість [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) |  |

## Зміст

-   [MongoDB\\Driver\\Exception\\WriteException::getWriteResult](mongodb-driver-writeexception.getwriteresult.html) — Повертає WriteResult для операції запису помилкою, що закінчилася.