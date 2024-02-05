---
navigation:
  - class.parseerror.md: « ParseError
  - class.valueerror.md: ValueError »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: TypeError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TypeError

(PHP 7, PHP 8)

## Вступ

Исключение**TypeError** може бути викинуто, якщо:

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

## список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Исключение**TypeError** більше не викидається, коли у вбудовану PHP-функцію у режимі strict type передається неприпустима кількість аргументів. Натомість викидається [ArgumentCountError](class.argumentcounterror.md) |
