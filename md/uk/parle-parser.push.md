---
navigation:
  - parle-parser.precedence.md: '« Parle\\Parser::precedence'
  - parle-parser.reset.md: 'Parle\\Parser::reset »'
  - index.md: PHP Manual
  - class.parle-parser.md: Parle\\Parser
title: 'Parle\\Parser::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\Parser::push

(PECL parle >= 0.5.1)

Parle\\Parser::push — Додає граматичне правило

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
