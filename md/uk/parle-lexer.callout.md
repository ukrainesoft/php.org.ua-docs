---
navigation:
  - parle-lexer.build.md: '« ParleLexer::build'
  - parle-lexer.consume.md: 'ParleLexer::consume »'
  - index.md: PHP Manual
  - class.parle-lexer.md: ParleLexer
title: 'ParleLexer::callout'
---
# ParleLexer::callout

(PECL parle >= 0.7.2)

ParleLexer::callout - Визначає callback-функцію токена

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
