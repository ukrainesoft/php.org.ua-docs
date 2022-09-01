---
navigation:
  - parle-rparser.right.html: '« ParleRParser::right'
  - parle-rparser.token.html: 'ParleRParser::token »'
  - index.md: PHP Manual
  - class.parle-rparser.html: ParleRParser
title: 'ParleRParser::sigil'
---
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
