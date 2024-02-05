---
navigation:
  - parle-parser.right.md: '« Parle\\Parser::right'
  - parle-parser.sigilcount.md: 'Parle\\Parser::sigilCount »'
  - index.md: PHP Manual
  - class.parle-parser.md: Parle\\Parser
title: 'Parle\\Parser::sigil'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\Parser::sigil

(PECL parle >= 0.5.1)

Parle\\Parser::sigil — Витягує частину збігу за правилом

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
