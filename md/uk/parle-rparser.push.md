---
navigation:
  - parle-rparser.precedence.md: '« Parle\\RParser::precedence'
  - parle-rparser.reset.md: 'Parle\\RParser::reset »'
  - index.md: PHP Manual
  - class.parle-rparser.md: Parle\\RParser
title: 'Parle\\RParser::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\RParser::push

(PECL parle >= 0.7.0)

Parle\\RParser::push — Додає граматичне правило

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
