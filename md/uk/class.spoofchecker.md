---
navigation:
  - resourcebundle.locales.md: '« ResourceBundle::getLocales'
  - spoofchecker.areconfusable.md: 'Spoofchecker::areConfusable »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас Spoofchecker
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Spoofchecker

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

## Вступ

Цей клас існує тому, що Unicode містить велику кількість символів і включає різні системи письма з усього світу і їх некоректне використання може зробити програми і системи вразливими до атак хакерів, що використовують подібність символів.

Методи, що надаються, дозволяють перевірити рядок на предмет спроб обдурити користувача (`spoof detection`), наприклад, вставити в слово "pаypаl" кириличний символ 'а'.

## Огляд класів

```classsynopsis

    
     class Spoofchecker
     {

    /* Константы */
    
     public
     const
     int
      SINGLE_SCRIPT_CONFUSABLE;

    public
     const
     int
      MIXED_SCRIPT_CONFUSABLE;

    public
     const
     int
      WHOLE_SCRIPT_CONFUSABLE;

    public
     const
     int
      ANY_CASE;

    public
     const
     int
      SINGLE_SCRIPT;

    public
     const
     int
      INVISIBLE;

    public
     const
     int
      CHAR_LIMIT;

    public
     const
     int
      ASCII;

    public
     const
     int
      HIGHLY_RESTRICTIVE;

    public
     const
     int
      MODERATELY_RESTRICTIVE;

    public
     const
     int
      MINIMALLY_RESTRICTIVE;

    public
     const
     int
      UNRESTRICTIVE;

    public
     const
     int
      SINGLE_SCRIPT_RESTRICTIVE;

    public
     const
     int
      MIXED_NUMBERS;

    public
     const
     int
      HIDDEN_OVERLAY;


    /* Методы */
    
   public __construct()

    public areConfusable(string $string1, string $string2, int &$errorCode = null): bool
public isSuspicious(string $string, int &$errorCode = null): bool
public setAllowedLocales(string $locales): void
public setChecks(int $checks): void
public setRestrictionLevel(int $level): void

   }
```

## Обумовлені константи

**`Spoofchecker::SINGLE_SCRIPT_CONFUSABLE`**

**`Spoofchecker::MIXED_SCRIPT_CONFUSABLE`**

**`Spoofchecker::WHOLE_SCRIPT_CONFUSABLE`**

**`Spoofchecker::ANY_CASE`**

**`Spoofchecker::SINGLE_SCRIPT`**

**`Spoofchecker::INVISIBLE`**

**`Spoofchecker::CHAR_LIMIT`**

**`Spoofchecker::ASCII`**

**`Spoofchecker::HIGHLY_RESTRICTIVE`**

**`Spoofchecker::MODERATELY_RESTRICTIVE`**

**`Spoofchecker::MINIMALLY_RESTRICTIVE`**

**`Spoofchecker::UNRESTRICTIVE`**

**`Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE`**

**`Spoofchecker::MIXED_NUMBERS`**

**`Spoofchecker::HIDDEN_OVERLAY`**

## список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Додані константи класу, які використовуються [Spoofchecker::setRestrictionLevel()](spoofchecker.setrestrictionlevel.md), такі як: **`Spoofchecker::ASCII`** **`Spoofchecker::HIGHLY_RESTRICTIVE`** **`Spoofchecker::MODERATELY_RESTRICTIVE`** **`Spoofchecker::MINIMALLY_RESTRICTIVE`** **`Spoofchecker::UNRESTRICTIVE`** **`Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE`** |

## Зміст

-   [Spoofchecker::areConfusable](spoofchecker.areconfusable.md)— Перевірити, чи є рядки підозрілими
-   [Spoofchecker::\_\_construct](spoofchecker.construct.md) \- Конструктор класу
-   [Spoofchecker::isSuspicious](spoofchecker.issuspicious.md)— Перевіряє, чи текст містить підозрілі символи
-   [Spoofchecker::setAllowedLocales](spoofchecker.setallowedlocales.md)— Локаль для використання у перевірках
-   [Spoofchecker::setChecks](spoofchecker.setchecks.md)— Встановити набір перевірок
-   [Spoofchecker::setRestrictionLevel](spoofchecker.setrestrictionlevel.md) \- Встановлює рівень обмеження
