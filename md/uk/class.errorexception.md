---
navigation:
  - exception.clone.md: '« Exception::\_\_clone'
  - errorexception.construct.md: 'ErrorException::\_\_construct »'
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: ErrorException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ErrorException

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

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
    
   public __construct(    string $message = "",    int $code = 0,    int $severity = E_ERROR,    ?string $filename = null,    ?int $line = null,    ?Throwable $previous = null)

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

**Пример #1 Использование[set\_error\_handler()](function.set-error-handler.md) змінити повідомлення про помилки в ErrorException.**

```php
<?php
function exception_error_handler(int $errno, string $errstr, string $errfile = null, int $errline) {
    if (!(error_reporting() & $errno)) {
        // Этот код ошибки не входит в error_reporting
        return;
    }
    throw new \ErrorException($errstr, 0, $errno, $errfile, $errline);
}
set_error_handler(exception_error_handler(...));
// До PHP 8.1.0 и введения синтаксиса callback-функции как объекта первого класса вместо этого необходимо использовать следующий вызов:
// set_error_handler(__NAMESPACE__ . "\\exception_error_handler");

/* вызываем исключение */
strpos();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Fatal error: Uncaught exception 'ErrorException' with message 'strpos() expects at least 2 parameters, 0 given' in /home/bjori/tmp/ex.php:12
Stack trace:
#0 [internal function]: exception_error_handler(2, 'strpos() expect...', '/home/bjori/php...', 12, Array)
#1 /home/bjori/php/cleandocs/test.php(12): strpos()
#2 {main}
  thrown in /home/bjori/tmp/ex.php on line 12
```

## Зміст

-   [ErrorException::\_\_construct](errorexception.construct.md) \- Створює виняток
-   [ErrorException::getSeverity](errorexception.getseverity.md)— Отримує серйозність виключення
