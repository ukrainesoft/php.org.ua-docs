---
navigation:
  - parle-parser.nonassoc.md: '« ParleParser::nonassoc'
  - parle-parser.push.md: 'ParleParser::push »'
  - index.md: PHP Manual
  - class.parle-parser.md: ParleParser
title: 'ParleParser::precedence'
---
# ParleParser::precedence

(PECL parle >= 0.5.1)

ParleParser::precedence — Оголошує правило пріоритету

### Опис

```methodsynopsis
public Parle\Parser::precedence(string $tok): void
```

Оголошує правило пріоритету фіктивного термінального символу. Правило може бути пізніше використане у спеціальних правилах граматики.

### Список параметрів

`tok`

Ім'я токена.

### Значення, що повертаються

Функція не повертає значення після виконання.
