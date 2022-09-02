---
navigation:
  - parle-parser.right.md: '« ParleParser::right'
  - parle-parser.token.md: 'ParleParser::token »'
  - index.md: PHP Manual
  - class.parle-parser.md: ParleParser
title: 'ParleParser::sigil'
---
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
