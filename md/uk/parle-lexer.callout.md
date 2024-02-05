---
navigation:
  - parle-lexer.build.md: '« Parle\\Lexer::build'
  - parle-lexer.consume.md: 'Parle\\Lexer::consume »'
  - index.md: PHP Manual
  - class.parle-lexer.md: Parle\\Lexer
title: 'Parle\\Lexer::callout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\Lexer::callout

(PECL parle >= 0.7.2)

Parle\\Lexer::callout - Визначає callback-функцію токена

### Опис

```methodsynopsis
public Parle\Lexer::callout(int $id, callable $callback): void
```

Визначає callback-функцію, яка буде викликатись, коли лексер зустрічає певний токен.

### Список параметрів

`id`

Ідентифікатор токена.

`callback`

Callable для дзвінка. Об'єкт, що викликається, не отримує аргументів, а його значення, що повертається, ігнорується.

### Значення, що повертаються

Функція не повертає значення після виконання.
