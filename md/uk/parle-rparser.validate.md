---
navigation:
  - parle-rparser.trace.md: '« Parle\\RParser::trace'
  - class.parle-stack.md: Parle\\Stack »
  - index.md: PHP Manual
  - class.parle-rparser.md: Parle\\RParser
title: 'Parle\\RParser::validate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\RParser::validate

(PECL parle >= 0.7.0)

Parle\\RParser::validate — Перевіряє вхідні дані

### Опис

```methodsynopsis
public Parle\RParser::validate(string $data, Parle\RLexer $lexer): bool
```

Перевіряє вхідний рядок. Рядок аналізується внутрішнім механізмом, тому метод корисний швидкої перевірки вхідних даних.

### Список параметрів

`data`

Рядок для перевірки.

`lexer`

Об'єкт лексера містить правила лексування, підготовлені для конкретної граматики.

### Значення, що повертаються

Повертає логічне значення (bool) визначальне, чи вхідні дані відповідають заданим правилам чи ні.
