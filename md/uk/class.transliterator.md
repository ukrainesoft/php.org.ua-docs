---
navigation:
  - spoofchecker.setchecks.md: '« Spoofchecker::setChecks'
  - transliterator.construct.md: 'Transliterator::construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас Transliterator
---
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

-   [Transliterator::construct](transliterator.construct.md) - Приватний конструктор
-   [Transliterator::create](transliterator.create.md) - Створити транслітератор
-   [Transliterator::createFromRules](transliterator.createfromrules.md) - Створити транслітератор на основі правил
-   [Transliterator::createInverse](transliterator.createinverse.md) - Створити інвертований транслітератор
-   [Transliterator::getErrorCode](transliterator.geterrorcode.md) — Отримати код останньої помилки
-   [Transliterator::getErrorMessage](transliterator.geterrormessage.md) — Отримати останнє повідомлення про помилку
-   [Transliterator::listIDs](transliterator.listids.md) — Отримати ідентифікатори транслітератора
-   [Transliterator::transliterate](transliterator.transliterate.md) — Транслітерувати рядок
