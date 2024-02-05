---
navigation:
  - eventutil.sslrandpoll.md: '« EventUtil::sslRandPoll'
  - book.ftp.md: FTP »
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EventException

(No version information available, might only be in Git)

## Вступ

Исключение**EventException** викидається, коли методи модуля Event виявляють неприпустиме введення користувача або виявляють невиправну помилку. Цей виняток сигналізує розробникам у тому, що потрібно коректно обробляти виняткові ситуації.

## Огляд класів

```classsynopsis

    
     class EventException
    

    
     extends
      RuntimeException
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
    
   public Error::__construct(string $message = "", int $code = 0, ?Throwable $previous = null)

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
