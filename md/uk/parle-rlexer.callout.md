---
navigation:
  - parle-rlexer.build.md: '« Parle\\RLexer::build'
  - parle-rlexer.consume.md: 'Parle\\RLexer::consume »'
  - index.md: PHP Manual
  - class.parle-rlexer.md: Parle\\RLexer
title: 'Parle\\RLexer::callout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\RLexer::callout

(PECL parle >= 0.7.2)

Parle\\RLexer::callout - Визначає callback-функцію токена

### Опис

```methodsynopsis
public Parle\RLexer::callout(int $id, callable $callback): void
```

Визначає callback-функцію, яка буде викликатись, коли лексер зустрічає певний токен.

### Список параметрів

`id`

Token id.

`callback`

Callable-функція. Об'єкт, що викликається, не отримує аргументів, а його значення, що повертається, ігнорується.

### Значення, що повертаються

Функція не повертає значення після виконання.
