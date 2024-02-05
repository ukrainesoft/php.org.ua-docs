---
navigation:
  - internaliterator.valid.md: '« InternalIterator::valid'
  - throwable.getmessage.md: 'Throwable::getMessage »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Throwable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Throwable

(PHP 7, PHP 8)

## Вступ

**Throwable** є батьківським інтерфейсом для всіх об'єктів, що викидаються за допомогою виразу [`throw`](language.exceptions.md), включаючи класи [Error](class.error.md) і [Exception](class.exception.md)

> **Зауваження** :
> 
> Класи PHP не можуть безпосередньо реалізувати інтерфейс **Throwable**. Натомість вони можуть успадковувати підклас [Exception](class.exception.md)

## Огляд інтерфейсів

```classsynopsis

    
     interface Throwable

    extends
      Stringable {

    /* Методы */
    
   public getMessage(): string
public getCode(): int
public getFile(): string
public getLine(): int
public getTrace(): array
public getTraceAsString(): string
public getPrevious(): ?Throwable
public __toString(): string


    /* Наследуемые методы */
    public Stringable::__toString(): string

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Класс**Throwable** тепер реалізує інтерфейс [Stringable](class.stringable.md) |

## Зміст

-   [Throwable::getMessage](throwable.getmessage.md)— Отримує повідомлення помилки
-   [Throwable::getCode](throwable.getcode.md)— Повертає код виключення
-   [Throwable::getFile](throwable.getfile.md)— Повертає файл, у якому викинуто виняток
-   [Throwable::getLine](throwable.getline.md)— Отримує рядок скрипта, в якому цей об'єкт було викинуто
-   [Throwable::getTrace](throwable.gettrace.md)— Повертає трасування стека
-   [Throwable::getTraceAsString](throwable.gettraceasstring.md)— Отримує результати трасування стека у вигляді рядка
-   [Throwable::getPrevious](throwable.getprevious.md)— Повертає попередній Throwable
-   [Throwable::\_\_function toString() { \[native code\] }](throwable.tostring.md)— Отримує рядкову виставу викинутого об'єкта
