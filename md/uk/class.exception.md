---
navigation:
  - reserved.exceptions.md: « Зумовлені винятки
  - exception.construct.md: 'Exception::\_\_construct »'
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: Exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Exception

(PHP 5, PHP 7, PHP 8)

## Вступ

**Exception** — це базовий клас для всіх винятків користувача.

## Огляд класів

```classsynopsis

     
      class Exception
     

     
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

Текст виключення

code

Код виключення

file

Ім'я файлу, в якому було викликано виняток

line

Номер рядка, в якому було викликано виняток

previous

Раніше викинутий виняток

string

Строкове представлення трасування стека

trace

Трасування стека у вигляді масиву

## Зміст

-   [Exception::\_\_construct](exception.construct.md) \- Створити виняток
-   [Exception::getMessage](exception.getmessage.md)— Отримує повідомлення про виключення
-   [Exception::getPrevious](exception.getprevious.md)— Повертає попередній об'єкт, що реалізує Throwable
-   [Exception::getCode](exception.getcode.md)— Отримує код виключення
-   [Exception::getFile](exception.getfile.md)— Отримує файл, у якому виник виняток
-   [Exception::getLine](exception.getline.md)— Отримує рядок, у якому виник виняток
-   [Exception::getTrace](exception.gettrace.md)— Отримує трасування стека
-   [Exception::getTraceAsString](exception.gettraceasstring.md)— Отримує трасування стека у вигляді рядка
-   [Exception::\_\_function toString() { \[native code\] }](exception.tostring.md)— Строкове подання винятку
-   [Exception::\_\_clone](exception.clone.md)— Клонувати виняток
