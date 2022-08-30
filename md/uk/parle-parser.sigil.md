Витягує частину збігу за правилом

-   [« ParleParser::right](parle-parser.right.html)
    
-   [ParleParser::token »](parle-parser.token.html)
    
-   [PHP Manual](index.html)
    
-   [ParleParser](class.parle-parser.html)
    
-   Витягує частину збігу за правилом
    

# ParleParser::sigil

(PECL parle >= 0.5.1)

ParleParser::sigil — Витягує частину збігу за правилом

### Опис

```methodsynopsis
public Parle\Parser::sigil(int $idx): string
```

Повертає частину збігу за правилом. Метод еквівалентний функціональності псевдозмінних у Bison.

### Список параметрів

`idx`

Індекс збігу, що відраховується від нуля.

### Значення, що повертаються

Повертає рядок (string) з частиною, що збігається.