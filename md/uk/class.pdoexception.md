Клас PDOException

-   [« PDOStatement::setFetchMode](pdostatement.setfetchmode.html)
    
-   [Драйверы PDO »](pdo.drivers.html)
    
-   [PHP Manual](index.html)
    
-   [PDO](book.pdo.html)
    
-   Клас PDOException
    

# Клас PDOException

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Помилка, викликана PDO. Вам не слід викидати винятки **PDOException** зі свого коду. Для додаткової інформації про винятки в PHP дивіться розділ [Исключения](language.exceptions.html)

## Огляд класів

```classsynopsis

     
    

    
     
      class PDOException
     

     
      extends
       RuntimeException
     
     {

    /* Свойства */
    
     protected
     int|string
      $code;

    public
     ?array
      $errorInfo = null;


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

## Властивості

errorInfo

Відповідає [PDO::errorInfo()](pdo.errorinfo.html) або [PDOStatement::errorInfo()](pdostatement.errorinfo.html)

code

Код помилки `SQLSTATE`. Щоб його отримати, використовуйте [Exception::getCode()](exception.getcode.html)