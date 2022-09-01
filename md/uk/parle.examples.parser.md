---
navigation:
  - parle.examples.lexer.html: « Приклади використання лексера
  - class.parle-lexer.html: ParleLexer »
  - index.html: PHP Manual
  - parle.examples.html: Приклади
title: Приклад використання парсеру
---
## Приклад використання парсеру

**Приклад #1 Простий калькулятор**

```php
<?php

use Parle\{Parser, ParserException, Lexer, Token};

$p = new Parser;
$p->token("INTEGER");
$p->left("'+' '-' '*' '/'");

$p->push("start", "exp");
$prod_add = $p->push("exp", "exp '+' exp");
$prod_sub = $p->push("exp", "exp '-' exp");
$prod_mul = $p->push("exp", "exp '*' exp");
$prod_div = $p->push("exp", "exp '/' exp");
$p->push("exp", "INTEGER"); /* Индекс производства не используется. */

$p->build();

$lex = new Lexer;
$lex->push("[+]", $p->tokenId("'+'"));
$lex->push("[-]", $p->tokenId("'-'"));
$lex->push("[*]", $p->tokenId("'*'"));
$lex->push("[/]", $p->tokenId("'/'"));
$lex->push("\\d+", $p->tokenId("INTEGER"));
$lex->push("\\s+", Token::SKIP);

$lex->build();

$exp = array(
    "1 + 1",
    "33 / 10",
    "100 * 45",
    "17 - 45",
);

foreach ($exp as $in) {
    if (!$p->validate($in, $lex)) {
        throw new ParserException("Не удалось проверить ввод");
    }

    $p->consume($in, $lex);

    while (Parser::ACTION_ERROR != $p->action && Parser::ACTION_ACCEPT != $p->action) {
        switch ($p->action) {
            case Parser::ACTION_ERROR:
                throw new ParserException("Parser error");
                break;
            case Parser::ACTION_SHIFT:
            case Parser::ACTION_GOTO:
            case Parser::ACTION_ACCEPT:
                break;
            case Parser::ACTION_REDUCE:
                switch ($p->reduceId) {
                    case $prod_add:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                        echo "$l + $r = " . ($l + $r) . "\n";
                        break;
                    case $prod_sub:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                        echo "$l - $r = " . ($l - $r) . "\n";
                        break;
                    case $prod_mul:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                        echo "$l * $r = " . ($l * $r) . "\n";
                        break;
                    case $prod_div:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                    echo "$l / $r = " . ($l / $r) . "\n";
                        break;
            }
            break;
        }
        $p->advance();
    }
}
```

**Приклад #2 Розібрати слова з речення**

```php
<?php

use Parle\{Lexer, Token, Parser, ParserException};

$p = new Parser;
$p->token("WORD");
$p->push("START", "SENTENCE");
$p->push("SENTENCE", "WORDS");
$prod_word_0 = $p->push("WORDS", "WORDS WORD");
$prod_word_1 = $p->push("WORDS", "WORD");
$p->build();

$lex = new Lexer;
$lex->push("[^\s]{-}[\.,\:\;\?]+", $p->tokenId("WORD"));
$lex->push("[\s\.,\:\;\?]+", Token::SKIP);
$lex->build();

$in = "Dis-moi où est ton papa?";
$p->consume($in, $lex);
do {
    switch ($p->action) {
    case Parser::ACTION_ERROR:
        throw new ParserException("Error");
        break;
    case Parser::ACTION_SHIFT:
    case Parser::ACTION_GOTO:
        /* var_dump($p->trace());*/
        break;
    case Parser::ACTION_REDUCE:
        $rid = $p->reduceId();
        if ($rid == $prod_word_1) {
            var_dump($p->sigil(0));
        } if ($rid == $prod_word_0) {
            var_dump($p->sigil(1));
        }
        break;
    }
    $p->advance();
} while (Parser::ACTION_ACCEPT != $p->action);
```
