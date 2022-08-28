ValueError

-   [« TypeError](class.typeerror.html)
    
-   [UnhandledMatchError »](class.unhandledmatcherror.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые исключения](reserved.exceptions.html)
    
-   ValueError
    

# ValueError

(PHP 8)

## Вступ

Помилка **ValueError** викидається, якщо тип аргументу правильний, але його значення неправильне. Наприклад, передача негативного цілого числа, коли функція очікує на позитивне, або передача порожнього рядка/масиву, коли функція очікує, що він не буде порожнім.

## Огляд класів

```classsynopsis

     
    

    
     
      class ValueError
     

     
      extends
       Error
     
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