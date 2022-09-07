---
navigation:
  - parle-lexer.insertmacro.md: '« ParleLexer::insertMacro'
  - parle-lexer.reset.md: 'ParleLexer::reset »'
  - index.md: PHP Manual
  - class.parle-lexer.md: ParleLexer
title: 'ParleLexer::push'
---
# ParleLexer::push

(PECL parle >= 0.5.1)

ParleLexer::push - Додає правило лексера

### Опис

```methodsynopsis
public Parle\Lexer::push(string $regex, int $id): void
```

Висуває шаблон для розпізнавання лексеми.

### Список параметрів

`regex`

Регулярне вираз, використовуване зіставлення токенів.

`id`

Ідентифікатор токена. Якщо екземпляр лексера призначений для автономного використання, то може бути довільним числом. Якщо екземпляр лексера буде переданий синтаксичному аналізатору, має бути ідентифікатор, який повертається [ParleParser::tokenid()](parle-parser.tokenid.md)

### Значення, що повертаються

Функція не повертає значення після виконання.
