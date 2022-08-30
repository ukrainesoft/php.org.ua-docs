Приклади використання лексера

-   [« Приклади](parle.examples.md)
    
-   [Пример использования парсера »](parle.examples.parser.md)
    
-   [PHP Manual](index.md)
    
-   [Приклади](parle.examples.md)
    
-   Приклади використання лексера
    

## Приклади використання лексера

**Приклад #1 Токенізація списку цілих чисел через кому**

```php
<?php

use Parle\Token;
use Parle\Lexer;
use Parle\LexerException;

/* name => id */
$token = array(
        "COMMA" => 1,
        "CRLF" => 2,
        "DECIMAL" => 3,
);
/* id => name */
$tokenIdToName = array_flip($token);

$lex = new Lexer;
$lex->push("[\x2c]", $token["COMMA"]);
$lex->push("[\r][\n]", $token["CRLF"]);
$lex->push("[\d]+", $token["DECIMAL"]);
$lex->build();

$in = "0,1,2\r\n3,42,5\r\n6,77,8\r\n";

$lex->consume($in);

do {
        $lex->advance();
        $tok = $lex->getToken();

        if (Token::UNKNOWN == $tok->id) {
                throw new LexerException("Неизвестный токен '{$tok->value}' по смещению {$lex->marker}.");
        }

        echo "ТОКЕН: ", $tokenIdToName[$tok->id], PHP_EOL;
} while (Token::EOI != $tok->id);
```

**Приклад #2 Токенізувати оператор присвоєння**

```php
<?php

use Parle\{Token, Lexer};

$lex = new Lexer;

$lex->push("\$[a-zA-Z_][a-zA-Z0-9_]*", 1);
$lex->push("=", 2);
$lex->push("\d+", 3);
$lex->push(";", 4);

$lex->build();

$lex->consume('$x = 42; $y = 24;');


do {
    $lex->advance();
    $tok = $lex->getToken();
    var_dump($tok);
} while (Token::EOI != $tok->id);
```