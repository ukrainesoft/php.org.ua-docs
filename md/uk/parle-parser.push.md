---
navigation:
  - parle-parser.precedence.md: '« ParleParser::precedence'
  - parle-parser.reset.md: 'ParleParser::reset »'
  - index.md: PHP Manual
  - class.parle-parser.md: ParleParser
title: 'ParleParser::push'
---
# ParleParser::push

(PECL parle >= 0.5.1)

ParleParser::push — Додає граматичне правило

### Опис

```methodsynopsis
public Parle\Parser::push(string $name, string $rule): int
```

Додає граматичне правило. Повернений виробничий ідентифікатор може бути використаний пізніше у процесі синтаксичного аналізу, щоб ідентифікувати відповідність правилу.

### Список параметрів

`name`

Ім'я правила.

`rule`

Правило, яке буде додано. Синтаксис сумісний із Bison.

### Значення, що повертаються

Повертає ціле число (int), що представляє індекс правила.
