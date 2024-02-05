---
navigation:
  - parle-parser.trace.md: '« Parle\\Parser::trace'
  - class.parle-rparser.md: Parle\\RParser »
  - index.md: PHP Manual
  - class.parle-parser.md: Parle\\Parser
title: 'Parle\\Parser::validate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\Parser::validate

(PECL parle >= 0.5.1)

Parle\\Parser::validate — Перевіряє вхідні дані

### Опис

```methodsynopsis
public Parle\Parser::validate(string $data, Parle\Lexer $lexer): bool
```

Перевіряє вхідний рядок. Рядок аналізується усередині, тому метод корисний для швидкої перевірки введення.

### Список параметрів

`data`

Рядок для перевірки.

`lexer`

Об'єкт лексера містить правила лексування, підготовлені для конкретної граматики.

### Значення, що повертаються

Повертає логічне значення (bool) залежно від цього, відповідають вхідні дані заданим правилам чи ні.
