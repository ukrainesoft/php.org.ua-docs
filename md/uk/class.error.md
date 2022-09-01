---
navigation:
  - errorexception.getseverity.md: '« ErrorException::getSeverity'
  - error.construct.md: 'Error::construct »'
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: Error
---
# Error

(PHP 7, PHP 8)

## Вступ

**Error** - базовий клас всім внутрішніх помилок PHP.

## Огляд класів

```classsynopsis

     
    

    
     
      class Error
     

     implements 
       Throwable {

    /* Свойства */
    
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
    
   public __construct(string $message = "", int $code = 0, ?Throwable $previous = null)

    final public getMessage(): string
final public getPrevious(): ?Throwable
final public getCode(): int
final public getFile(): string
final public getLine(): int
final public getTrace(): array
final public getTraceAsString(): string
public __toString(): string
private __clone(): void

   }
```

## Властивості

message

Повідомлення про помилку

code

Код помилки

file

Ім'я файлу, в якому сталася помилка

line

Номер рядка, в якому сталася помилка

previous

Раніше викинутий виняток

string

Строкове представлення трасування стека

trace

Трасування стека у вигляді масиву

## Зміст

-   [Error::construct](error.construct.md) - Створює об'єкт класу Error
-   [Error::getMessage](error.getmessage.md) — Отримує повідомлення про помилку
-   [Error::getPrevious](error.getprevious.md) — Повертає попередній Throwable
-   [Error::getCode](error.getcode.md) — Повертає код помилки
-   [Error::getFile](error.getfile.md) — Отримує файл, у якому сталася помилка
-   [Error::getLine](error.getline.md) — Отримує номер рядка, в якому сталася помилка
-   [Error::getTrace](error.gettrace.md) — Отримує трасування стека
-   [Error::getTraceAsString](error.gettraceasstring.md) — Отримує трасування стека у вигляді рядка
-   [Error::toString](error.tostring.md) — Строкове подання помилки
-   [Error::clone](error.clone.md) - Клонує помилку
