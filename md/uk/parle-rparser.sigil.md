---
navigation:
  - parle-rparser.right.md: '« Parle\\RParser::right'
  - parle-rparser.sigilcount.md: 'Parle\\RParser::sigilCount »'
  - index.md: PHP Manual
  - class.parle-rparser.md: Parle\\RParser
title: 'Parle\\RParser::sigil'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\RParser::sigil

(PECL parle >= 0.7.0)

Parle\\RParser::sigil — Витягує збігову частину за правилом

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
