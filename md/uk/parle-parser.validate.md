---
navigation:
  - parle-parser.trace.html: '« ParleParser::trace'
  - class.parle-rparser.html: ParleRParser »
  - index.html: PHP Manual
  - class.parle-parser.html: ParleParser
title: 'ParleParser::validate'
---
# ParleParser::validate

(PECL parle >= 0.5.1)

ParleParser::validate — Перевіряє вхідні дані

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
