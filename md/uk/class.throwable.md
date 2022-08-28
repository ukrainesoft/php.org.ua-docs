Throwable

-   [« IteratorAggregate::getIterator](iteratoraggregate.getiterator.html)
    
-   [Throwable::getMessage »](throwable.getmessage.html)
    
-   [PHP Manual](index.html)
    
-   [Встроенные интерфейсы и классы](reserved.interfaces.html)
    
-   Throwable
    

# Throwable

(PHP 7, PHP 8)

## Вступ

**Throwable** є батьківським інтерфейсом для всіх об'єктів, що викидаються за допомогою виразу [`throw`](language.exceptions.html), включаючи класи [Error](class.error.html) і [Exception](class.exception.html)

> **Зауваження**
> 
> Класи PHP не можуть безпосередньо реалізувати інтерфейс **Throwable**. Натомість вони можуть успадковувати підклас [Exception](class.exception.html)

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface Throwable
      extends
       Stringable
     
     {

    /* Методы */
    
   public getMessage(): string
public getCode(): int
public getFile(): string
public getLine(): int
public getTrace(): array
public getTraceAsString(): string
public getPrevious(): ?Throwable
abstract public __toString(): string


    /* Наследуемые методы */
    public Stringable::__toString(): string

   }
```

## список змін

| Версия | Описание                                                                        |
|--------|---------------------------------------------------------------------------------|
|        | Клас **Throwable** тепер реалізує інтерфейс [Stringable](class.stringable.html) |

## Зміст

-   [Throwable::getMessage](throwable.getmessage.html) — Отримує повідомлення помилки
-   [Throwable::getCode](throwable.getcode.html) — Повертає код виключення
-   [Throwable::getFile](throwable.getfile.html) — Повертає файл, у якому викинуто виняток
-   [Throwable::getLine](throwable.getline.html) — Отримує рядок скрипта, в якому цей об'єкт було викинуто
-   [Throwable::getTrace](throwable.gettrace.html) — Повертає трасування стека
-   [Throwable::getTraceAsString](throwable.gettraceasstring.html) — Отримує результати трасування стека у вигляді рядка
-   [Throwable::getPrevious](throwable.getprevious.html) — Повертає попередній Throwable
-   [Throwable::\_\_toString](throwable.tostring.html) — Отримує рядкову виставу викинутого об'єкта