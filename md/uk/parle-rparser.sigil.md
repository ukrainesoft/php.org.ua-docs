Витягує збігову частину за правилом

-   [« Parle\\RParser::right](parle-rparser.right.html)
    
-   [Parle\\RParser::token »](parle-rparser.token.html)
    
-   [PHP Manual](index.html)
    
-   [Parle\\RParser](class.parle-rparser.html)
    
-   Витягує збігову частину за правилом
    

# ParleRParser::sigil

(PECL parle >= 0.7.0)

ParleRParser::sigil — Витягує збігову частину за правилом

### Опис

```methodsynopsis
public Parle\RParser::sigil(int $idx = ?): string
```

Повертає частину збігу за правилом. Метод еквівалентний функціональності псевдозмінних у Bison.

### Список параметрів

`idx`

Індекс збігу, що відраховується від нуля.

### Значення, що повертаються

Повертає рядок (string) з частиною, що збігається.