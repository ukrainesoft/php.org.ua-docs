ParseError

-   [« CompileError](class.compileerror.md)
    
-   [TypeError »](class.typeerror.md)
    
-   [PHP Manual](index.md)
    
-   [Обумовлені винятки](reserved.exceptions.md)
    
-   ParseError
    

# ParseError

(PHP 7, PHP 8)

## Вступ

**ParseError** викидається, коли виникає помилка при розборі PHP-коду, наприклад, коли викликається функція [eval()](function.eval.md)

> **Зауваження**: Починаючи з PHP 7.3.0, клас **ParseError** успадковується від [CompileError](class.compileerror.md). Раніше цей клас розширював клас [Error](class.error.md)

## Огляд класів

```classsynopsis

     
    

    
     
      class ParseError
     

     
      extends
       CompileError
     
     {

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
    
   final public Error::getMessage(): string
final public Error::getPrevious(): ?Throwable
final public Error::getCode(): int
final public Error::getFile(): string
final public Error::getLine(): int
final public Error::getTrace(): array
final public Error::getTraceAsString(): string
public Error::__toString(): string
private Error::__clone(): void

   }
```