---
navigation:
  - spoofchecker.setrestrictionlevel.md: '« Spoofchecker::setRestrictionLevel'
  - transliterator.construct.md: 'Transliterator::\_\_construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас Transliterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
    
     public
     const
     int
      FORWARD;

    public
     const
     int
      REVERSE;


    /* Свойства */
    public
     readonly
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

id

## Обумовлені константи

**`Transliterator::FORWARD`**

**`Transliterator::REVERSE`**

## список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Властивість id тепер доступна лише читання. |

## Зміст

-   [Transliterator::\_\_construct](transliterator.construct.md) \- Приватний конструктор
-   [Transliterator::create](transliterator.create.md) \- Створити транслітератор
-   [Transliterator::createFromRules](transliterator.createfromrules.md) \- Створити транслітератор на основі правил
-   [Transliterator::createInverse](transliterator.createinverse.md) \- Створити інвертований транслітератор
-   [Transliterator::getErrorCode](transliterator.geterrorcode.md)— Отримати код останньої помилки
-   [Transliterator::getErrorMessage](transliterator.geterrormessage.md)— Отримати останнє повідомлення про помилку
-   [Transliterator::listIDs](transliterator.listids.md)— Отримати ідентифікатори транслітератора
-   [Transliterator::transliterate](transliterator.transliterate.md)— Транслітерувати рядок
