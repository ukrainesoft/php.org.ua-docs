---
navigation:
  - exception.clone.md: '« Exception::clone'
  - errorexception.construct.md: 'ErrorException::construct »'
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: ErrorException
---
# ErrorException

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Виняток у разі виникнення помилки.

## Огляд класів

```classsynopsis

     
    

    
     
      class ErrorException
     

     
      extends
       Exception
     
     {

    /* Свойства */
    
     protected
     int
      $severity = E_ERROR;


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


    /* Методы */
    
   public __construct(    string $message = "",    int $code = 0,    int $severity = E_ERROR,    ?string $filename = null,    ?int $line = null,    ?Throwable $previous = null)

    final public getSeverity(): int


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

severity

Серйозність виключення

## Приклади

**Приклад #1 Використання [seterrorhandler()](function.set-error-handler.md) змінити повідомлення про помилки в ErrorException.**

```php
<?php
function exception_error_handler($severity, $message, $file, $line) {
    if (!(error_reporting() & $severity)) {
        // Этот код ошибки не входит в error_reporting
        return;
    }
    throw new ErrorException($message, 0, $severity, $file, $line);
}
set_error_handler("exception_error_handler");

/* вызываем исключение */
strpos();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Fatal error: Uncaught exception 'ErrorException' with message 'strpos() expects at least 2 parameters, 0 given' in /home/bjori/tmp/ex.php:12
Stack trace:
#0 [internal function]: exception_error_handler(2, 'strpos() expect...', '/home/bjori/php...', 12, Array)
#1 /home/bjori/php/cleandocs/test.php(12): strpos()
#2 {main}
  thrown in /home/bjori/tmp/ex.php on line 12
```

## Зміст

-   [ErrorException::construct](errorexception.construct.md) - Створює виняток
-   [ErrorException::getSeverity](errorexception.getseverity.md) — Отримує серйозність виключення
