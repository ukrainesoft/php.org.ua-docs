---
navigation:
  - transports.unix.md: '« Unix-сокети: UNIX та UDG'
  - tokens.md: Список тегів (tokens) парсера »
  - index.md: PHP Manual
  - appendices.md: Програми
title: Таблиці порівняння типів PHP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Таблиці порівняння типів PHP

Наступні таблиці показують роботу PHP з [типами змінних](language.types.md) і [операторами порівняння](language.operators.comparison.md) як для вільних, так і для суворих порівнянь. Ця інформація також відноситься до розділу документації з [приведення типів](language.types.type-juggling.md). Написати цей розділ розробників PHP надихнули коментарі користувачів та робота над фреймворком [» BlueShoes](http://www.blueshoes.org/en/developer/php_cheat_sheet/)

Перед тим, як почати користуватися таблицями, важливо зрозуміти типи та їх значення. Нарімер, `«42»`— строка (string), а`42`— целое число (int). Значение\*\*`false`\*\* - Логічне значення (bool), а `«false»`— строка (string).

> **Зауваження** :
> 
> HTML-форми не передають цілі, дробові чи логічні змінні: вони передають лише рядки. З'ясувати, чи рядок можна через функцію [is\_numeric()](function.is-numeric.md)

> **Зауваження** :
> 
> Вираз `if ($x)`якщо змінна $x не визначена, згенерує помилку рівня **`E_NOTICE`**. Натомість користуються мовними конструкціями [empty()](function.empty.md) або [isset()](function.isset.md), та/або ініціалізують змінну.

> **Зауваження** :
> 
> Бувають арифметичні операції, що повертають значення, яке становить константа **`NAN`** (Not A Number, нечисло). Будь-яке суворе чи не суворе порівняння цього значення з будь-яким іншим, включаючи його самого, але виключаючи **`true`**, поверне **`false`**(т. е`NAN != NAN`и`NAN !== NAN`). Приклади операцій, що повертають **`NAN`** `sqrt(-1)` `asin(2)`и`acosh(0)`

**Порівняння типів змінної $x та результатів функцій PHP, пов'язаних з типами**

| Выражение | [gettype()](function.gettype.md) | [empty()](function.empty.md) | [is\_null()](function.is-null.md) | [isset()](function.isset.md) | bool : `if($x)` |
| --- | --- | --- | --- | --- | --- |
| `$x = "";` | string | **`true`** | **`false`** | **`true`** | **`false`** |
| `$x = null;` | NULL | **`true`** | **`true`** | **`false`** | **`false`** |
| `var $x;` | NULL | **`true`** | **`true`** | **`false`** | **`false`** |
| $x не визначено | NULL | **`true`** | **`true`** | **`false`** | **`false`** |
| `$x = [];` | array | **`true`** | **`false`** | **`true`** | **`false`** |
| `$x = ['a', 'b'];` | array | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = false;` | bool | **`true`** | **`false`** | **`true`** | **`false`** |
| `$x = true;` | bool | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = 1;` | int | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = 42;` | int | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = 0;` | int | **`true`** | **`false`** | **`true`** | **`false`** |
| `$x = -1;` | int | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = "1";` | string | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = "0";` | string | **`true`** | **`false`** | **`true`** | **`false`** |
| `$x = "-1";` | string | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = "php";` | string | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = "true";` | string | **`false`** | **`false`** | **`true`** | **`true`** |
| `$x = "false";` | string | **`false`** | **`false`** | **`true`** | **`true`** |

**Гибкое сравнение через оператор`==`**

|  | **`true`** | **`false`** | `1` | `0` | `-1` | `"1"` | `"0"` | `"-1"` | **`null`** | `[]` | `"php"` | `""` |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **`true`** | **`true`** | **`false`** | **`true`** | **`false`** | **`true`** | **`true`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** |
| **`false`** | **`false`** | **`true`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** | **`true`** | **`true`** | **`false`** | **`true`** |
|  | **`true`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
|  | **`false`** | **`true`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** | **`true`** | **`false`** | **`false`**\* | **`false`**\* |
| `-1` | **`true`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"1"` | **`true`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"0"` | **`false`** | **`true`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"-1"` | **`true`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** |
| **`null`** | **`false`** | **`true`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`true`** | **`false`** | **`true`** |
| `[]` | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`true`** | **`false`** | **`false`** |
| `"php"` | **`true`** | **`false`** | **`false`** | **`false`**\* | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** |
| `""` | **`false`** | **`true`** | **`false`** | **`false`**\* | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`true`** |

\* \*\*`true`\*\*до PHP 8.0.0.

**Жорстке порівняння через оператор `===`**

|  | **`true`** | **`false`** | `1` | `0` | `-1` | `"1"` | `"0"` | `"-1"` | **`null`** | `[]` | `"php"` | `""` |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **`true`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
|  | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
|  | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `-1` | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"1"` | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"0"` | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"-1"` | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** | **`false`** |
| **`null`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** | **`false`** |
| `[]` | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** | **`false`** |
| `"php"` | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** | **`false`** |
| `""` | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`** |
