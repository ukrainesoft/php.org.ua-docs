- [«ResourceBundle::getLocales](resourcebundle.locales.md)
- [Spoofchecker::areConfusable »](spoofchecker.areconfusable.md)

- [PHP Manual](index.md)
- [intl](book.intl.md)
- Клас Spoofchecker

# Клас Spoofchecker

(PHP 5 = 5.4.0, PHP 7, PHP 8, PECL intl = 2.0.0)

## Вступ

Цей клас існує тому, що Unicode містить велику кількість
символів і включає різні системи письма з усього світу і їх
некоректне використання може зробити програми та системи вразливими до
хакерським атакам, що використовують схожість символів.

Методи, що надаються, дозволяють перевірити рядок на предмет спроб.
обдурити користувача (`spoof detection`), наприклад, вставити у слово
"pаypаl" кириличний символ 'а'.

## Огляд класів

class **Spoofchecker** {

/\* Constants \*/

const int\|float `ASCII` = 0x10000000;

const int\|float `HIGHLY_RESTRICTIVE` = 0x30000000;

const int\|float `MODERATELY_RESTRICTIVE` = 0x40000000;

const int\|float `MINIMALLY_RESTRICTIVE` = 0x50000000;

const int\|float `UNRESTRICTIVE` = 0x60000000;

const int\|float `SINGLE_SCRIPT_RESTRICTIVE` = 0x20000000;

const int `SINGLE_SCRIPT_CONFUSABLE` = 1;

const int `MIXED_SCRIPT_CONFUSABLE` = 2;

const int `WHOLE_SCRIPT_CONFUSABLE` = 4;

const int `ANY_CASE` = 8;

const int `SINGLE_SCRIPT` = 16;

const int `INVISIBLE` = 32;

const int `CHAR_LIMIT` = 64;

/\* Методи \*/

public [\_\_construct](spoofchecker.construct.md)()

public [areConfusable](spoofchecker.areconfusable.md)(string
`$string1`, string `$string2`, int `&$errorCode` = **`null`**): bool

public [isSuspicious](spoofchecker.issuspicious.md)(string `$string`,
int `&$errorCode` = **`null`**): bool

public [setAllowedLocales](spoofchecker.setallowedlocales.md)(string
`$locales`): void

public [setChecks](spoofchecker.setchecks.md)(int `$checks`): void

}

## Зумовлені константи

**`Spoofchecker::ASCII`**

**`Spoofchecker::HIGHLY_RESTRICTIVE`**

**`Spoofchecker::MODERATELY_RESTRICTIVE`**

**`Spoofchecker::MINIMALLY_RESTRICTIVE`**

**`Spoofchecker::UNRESTRICTIVE`**

**`Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE`**

**`Spoofchecker::SINGLE_SCRIPT_CONFUSABLE`**

**`Spoofchecker::MIXED_SCRIPT_CONFUSABLE`**

**`Spoofchecker::WHOLE_SCRIPT_CONFUSABLE`**

**`Spoofchecker::ANY_CASE`**

**`Spoofchecker::SINGLE_SCRIPT`**

**`Spoofchecker::INVISIBLE`**

**`Spoofchecker::CHAR_LIMIT`**

## Список змін

| Версія | Опис                                                                                                                                                                                                                                                                                                                           |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 7.3.0  | Додані константи класу, що використовуються **Spoofchecker::setRestrictionLevel()**, такі як: **Spoofchecker::ASCII**, **Spoofchecker::HIGHLY_RESTRICTIVE**, **Spoofchecker::MODERATELY_RESTRICTIVE* *, **Spoofchecker::MINIMALLY_RESTRICTIVE**, **Spoofchecker::UNRESTRICTIVE**, **Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE**. |

## Зміст

- [Spoofchecker::areConfusable](spoofchecker.areconfusable.md) -
Перевірити, чи є рядки підозрілими
- [Spoofchecker::\_\_construct](spoofchecker.construct.md) -
Конструктор класу
- [Spoofchecker::isSuspicious](spoofchecker.issuspicious.md) -
Перевіряє, чи текст містить підозрілі символи
- [Spoofchecker::setAllowedLocales](spoofchecker.setallowedlocales.md)
— Локаль для використання у перевірках
- [Spoofchecker::setChecks](spoofchecker.setchecks.md) — Встановити
набір перевірок
