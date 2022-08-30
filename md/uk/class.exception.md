Exception

-   [« Предопределённые исключения](reserved.exceptions.html)
    
-   [Exception::construct »](exception.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые исключения](reserved.exceptions.html)
    
-   Exception
    

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

-   [Exception::construct](exception.construct.html) - Створити виняток
-   [Exception::getMessage](exception.getmessage.html) — Отримує повідомлення про виключення
-   [Exception::getPrevious](exception.getprevious.html) — Повертає попередній об'єкт, що реалізує Throwable
-   [Exception::getCode](exception.getcode.html) — Отримує код виключення
-   [Exception::getFile](exception.getfile.html) — Отримує файл, у якому виник виняток
-   [Exception::getLine](exception.getline.html) — Отримує рядок, у якому виник виняток
-   [Exception::getTrace](exception.gettrace.html) — Отримує трасування стека
-   [Exception::getTraceAsString](exception.gettraceasstring.html) — Отримує трасування стека у вигляді рядка
-   [Exception::toString](exception.tostring.html) — Строкове подання винятку
-   [Exception::clone](exception.clone.html) — Клонувати виняток