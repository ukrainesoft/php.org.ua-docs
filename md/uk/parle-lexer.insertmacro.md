---
navigation:
  - parle-lexer.gettoken.html: '« ParleLexer::getToken'
  - parle-lexer.push.html: 'ParleLexer::push »'
  - index.html: PHP Manual
  - class.parle-lexer.html: ParleLexer
title: 'ParleLexer::insertMacro'
---
# ParleLexer::insertMacro

(PECL parle >= 0.5.1)

ParleLexer::insertMacro — Вставляє макрос регулярного виразу

### Опис

```methodsynopsis
public Parle\Lexer::insertMacro(string $name, string $regex): void
```

Вставляє макрос регулярного виразу, який можна використовувати як ярлик і включити до інших регулярних виразів.

### Список параметрів

`name`

Макрос ім'я.

`regex`

Регулярний вираз.

### Значення, що повертаються

Функція не повертає значення після виконання.
