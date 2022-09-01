---
navigation:
  - parle-lexer.insertmacro.html: '« ParleLexer::insertMacro'
  - parle-lexer.reset.html: 'ParleLexer::reset »'
  - index.html: PHP Manual
  - class.parle-lexer.html: ParleLexer
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

Ідентифікатор токена. Якщо екземпляр лексера призначений для автономного використання, то може бути довільним числом. Якщо екземпляр лексера буде переданий синтаксичному аналізатору, має бути ідентифікатор, який повертається [ParleParser::tokenid()](parle-parser.tokenid.html)

### Значення, що повертаються

Функція не повертає значення після виконання.
