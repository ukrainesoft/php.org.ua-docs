Клас Transliterator

-   [« Spoofchecker::setChecks](spoofchecker.setchecks.html)
    
-   [Transliterator::\_\_construct »](transliterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [intl](book.intl.html)
    
-   Клас Transliterator
    

# Клас Transliterator

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

## Вступ

Цей клас надає функціональність транслітерації рядків.

## Огляд класів

```classsynopsis

     
    

    
     
      class Transliterator
     
     {

    /* Константы */
    
     const
     int
      FORWARD = 0;

    const
     int
      REVERSE = 1;


    /* Свойства */
    public
     string
      $id;


    /* Методы */
    
   final private __construct()

    public static create(string $id, int $direction = Transliterator::FORWARD): ?Transliterator
public static createFromRules(string $rules, int $direction = Transliterator::FORWARD): ?Transliterator
public createInverse(): ?Transliterator
public getErrorCode(): int|false
public getErrorMessage(): string|false
public static listIDs(): array|false
public transliterate(string $string, int $start = 0, int $end = -1): string|false

   }
```

## Властивості

ід

## Обумовлені константи

**`Transliterator::FORWARD`**

**`Transliterator::REVERSE`**

## Зміст

-   [Transliterator::\_\_construct](transliterator.construct.html) - Приватний конструктор
-   [Transliterator::create](transliterator.create.html) - Створити транслітератор
-   [Transliterator::createFromRules](transliterator.createfromrules.html) - Створити транслітератор на основі правил
-   [Transliterator::createInverse](transliterator.createinverse.html) - Створити інвертований транслітератор
-   [Transliterator::getErrorCode](transliterator.geterrorcode.html) — Отримати код останньої помилки
-   [Transliterator::getErrorMessage](transliterator.geterrormessage.html) — Отримати останнє повідомлення про помилку
-   [Transliterator::listIDs](transliterator.listids.html) — Отримати ідентифікатори транслітератора
-   [Transliterator::transliterate](transliterator.transliterate.html) — Транслітерувати рядок