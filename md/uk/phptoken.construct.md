---
navigation:
  - class.phptoken.md: « PhpToken
  - phptoken.gettokenname.md: 'PhpToken::getTokenName »'
  - index.md: PHP Manual
  - class.phptoken.md: PhpToken
title: 'PhpToken::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PhpToken::\_\_construct

(PHP 8)

PhpToken::\_\_construct — Створює об'єкт PhpToken

### Опис

final public **PhpToken::\_\_construct**  
int`$id`,  
string`$text`,  
int`$line`  
int`$pos`  
) .

Повертає новий об'єкт PhpToken.

### Список параметрів

`id`

Одна з констант T\_\*(смотрите[Список тегів (tokens) парсера](tokens.md)), або символ ASCII, що представляє односимвольний токен.

`text`

Текстовий вміст токена.

`line`

Номер рядка (починаючи з 1), з якого починається токен.

`pos`

Початкова позиція (починаючи з 0) токена в рядку (кількість байтів).

### Дивіться також

-   [PhpToken::tokenize()](phptoken.tokenize.md) \- Розбирає заданий рядок, що містить програму на PHP, на масив об'єктів PhpToken
