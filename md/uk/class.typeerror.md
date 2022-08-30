TypeError

-   [« ParseError](class.parseerror.html)
    
-   [ValueError »](class.valueerror.html)
    
-   [PHP Manual](index.html)
    
-   [Обумовлені винятки](reserved.exceptions.html)
    
-   TypeError
    

# TypeError

(PHP 7, PHP 8)

## Вступ

Виняток **TypeError** може бути викинуто, якщо:

-   Значення, що встановлюється для якості класу, відповідає відповідному оголошеному типу властивості.
-   Тип аргументу, переданого функції, відповідає типу, оголошеному функції для цього аргументу.
-   Тип повернутих функцією значення не відповідає типу повернення, оголошеному у функції.

## Огляд класів

```classsynopsis

     
    

    
     
      class TypeError
     

     
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

## список змін

| Версия | Описание                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Виняток **TypeError** більше не викидається, коли у вбудовану PHP-функцію у режимі strict type передається неприпустима кількість аргументів. Натомість викидається [ArgumentCountError](class.argumentcounterror.html) |