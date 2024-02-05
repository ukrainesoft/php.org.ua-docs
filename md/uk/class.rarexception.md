---
navigation:
  - rarentry.tostring.md: '« RarEntry::\_\_function toString() { [native code] }'
  - rarexception.isusingexceptions.md: 'RarException::isUsingExceptions »'
  - index.md: PHP Manual
  - book.rar.md: Rar
title: Клас RarException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас RarException

(PECL rar >= 2.0.0)

## Вступ

Клас служить двом цілям: це тип винятків, переданих функціями і методами модуля RAR, що дозволяє за допомогою стандартних методів робити запит і визначати помилку роботи модуля незалежно від того, передаються винятки або видаються попередження.

Використовуються такі коди помилок:

-   \-1 - помилка поза бібліотекою UnRAR
-   11 - недостатньо пам'яті
-   12 - неправильні дані
-   13 – неправильний архів
-   14 – невідомий формат
-   15 - помилка відкриття файлу
-   16 - помилка створення файлу
-   17 - помилка закриття файлу
-   18 – помилка читання
-   19 - помилка запису
-   20 - надто маленький буфер
-   21 - невідома помилка RAR
-   22 - потрібен пароль

## Огляд класів

```classsynopsis



    
     
      final
      class RarException
     

     
      extends
       Exception
     
     {


    /* Методы */
    
   public static isUsingExceptions(): bool
public static setUsingExceptions(bool $using_exceptions): void


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

## Зміст

-   [RarException::isUsingExceptions](rarexception.isusingexceptions.md)— Перевірити, чи будуть функції повертати помилки або викидати винятки
-   [RarException::setUsingExceptions](rarexception.setusingexceptions.md)— Увімкнути чи вимкнути генерацію винятків замість повернення помилок
