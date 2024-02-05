---
navigation:
  - parle-lexer.insertmacro.md: '« Parle\\Lexer::insertMacro'
  - parle-lexer.reset.md: 'Parle\\Lexer::reset »'
  - index.md: PHP Manual
  - class.parle-lexer.md: Parle\\Lexer
title: 'Parle\\Lexer::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\Lexer::push

(PECL parle >= 0.5.1)

Parle\\Lexer::push - Додає правило лексера

### Опис

```methodsynopsis
public Parle\Lexer::push(string $regex, int $id): void
```

Висуває шаблон для розпізнавання лексеми.

### Список параметрів

`regex`

Регулярне вираз, використовуване зіставлення токенів.

`id`

Ідентифікатор токена. Якщо екземпляр лексера призначений для автономного використання, то може бути довільним числом. Якщо екземпляр лексера буде переданий синтаксичному аналізатору, має бути ідентифікатор, який повертається [Parle\\Parser::tokenid()](parle-parser.tokenid.md)

### Значення, що повертаються

Функція не повертає значення після виконання.
