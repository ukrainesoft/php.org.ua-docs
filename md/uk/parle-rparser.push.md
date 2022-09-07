---
navigation:
  - parle-rparser.precedence.md: '« ParleRParser::precedence'
  - parle-rparser.reset.md: 'ParleRParser::reset »'
  - index.md: PHP Manual
  - class.parle-rparser.md: ParleRParser
title: 'ParleRParser::push'
---
# ParleRParser::push

(PECL parle >= 0.7.0)

ParleRParser::push — Додає граматичне правило

### Опис

```methodsynopsis
public Parle\RParser::push(string $name, string $rule): int
```

Додає граматичне правило. Повернений ідентифікатор може бути використаний пізніше у процесі синтаксичного аналізу, щоб ідентифікувати відповідність правилу.

### Список параметрів

`name`

Ім'я правила.

`rule`

Правило, яке буде додано. Синтаксис сумісний із Bison.

### Значення, що повертаються

Повертає ціле число (int), що представляє індекс правила.
