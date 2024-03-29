---
navigation:
  - class.pdorow.md: « PDORow
  - pdo.drivers.md: Драйвери PDO »
  - index.md: PHP Manual
  - book.pdo.md: PDO
title: Клас PDOException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас PDOException

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Помилка, викликана PDO. Вам не слід викидати винятки **PDOException** зі свого коду. Для додаткової інформації про винятки в PHP дивіться розділ [Винятки](language.exceptions.md)

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
    
   public Exception::__construct(string $message = "", int $code = 0, ?Throwable $previous = null)

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

Відповідає [PDO::errorInfo()](pdo.errorinfo.md) або [PDOStatement::errorInfo()](pdostatement.errorinfo.md)

code

Код ошибки`SQLSTATE`. Щоб його отримати, використовуйте [Exception::getCode()](exception.getcode.md)
