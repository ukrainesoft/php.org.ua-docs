---
navigation:
  - parle-rparser.right.md: '« ParleRParser::right'
  - parle-rparser.token.md: 'ParleRParser::token »'
  - index.md: PHP Manual
  - class.parle-rparser.md: ParleRParser
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
