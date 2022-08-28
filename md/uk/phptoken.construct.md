Створює об'єкт PhpToken

-   [« PhpToken](class.phptoken.html)
    
-   [PhpToken::getTokenName »](phptoken.gettokenname.html)
    
-   [PHP Manual](index.html)
    
-   [PhpToken](class.phptoken.html)
    
-   Створює об'єкт PhpToken
    

# PhpToken::construct

(PHP 8)

PhpToken::construct — Створює об'єкт PhpToken

### Опис

final public **PhpToken::construct**  
int `$id`  
string `$text`  
int `$line`  
int `$pos`  

Повертає новий об'єкт PhpToken.

### Список параметрів

`id`

Одна з констант T (дивіться [Список меток (tokens) парсера](tokens.html)), або символ ASCII, що представляє односимвольний токен.

`text`

Текстовий вміст токена.

`line`

Номер рядка (починаючи з 1), з якого починається токен.

`pos`

Початкова позиція (починаючи з 0) токена у рядку.

### Дивіться також

-   [PhpToken::tokenize()](phptoken.tokenize.html) - Розбирає заданий рядок, що містить програму на PHP, на масив об'єктів PhpToken