---
navigation:
  - parle-rlexer.gettoken.md: '« ParleRLexer::getToken'
  - parle-rlexer.push.md: 'ParleRLexer::push »'
  - index.md: PHP Manual
  - class.parle-rlexer.md: ParleRLexer
title: 'ParleRLexer::insertMacro'
---
# ParleRLexer::insertMacro

(PECL parle >= 0.5.1)

ParleRLexer::insertMacro — Вставляє макрос регулярного виразу

### Опис

```methodsynopsis
public Parle\RLexer::insertMacro(string $name, string $regex): void
```

Вставляє макрос регулярного виразу, який згодом можна використовувати як ярлик і включати до інших регулярних виразів.

### Список параметрів

`name`

Ім'я макросу

`regex`

Регулярний вираз.

### Значення, що повертаються

Функція не повертає значення після виконання.
