---
navigation:
  - parle-lexer.advance.md: '« Parle\\Lexer::advance'
  - parle-lexer.callout.md: 'Parle\\Lexer::callout »'
  - index.md: PHP Manual
  - class.parle-lexer.md: Parle\\Lexer
title: 'Parle\\Lexer::build'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\Lexer::build

(PECL parle >= 0.5.1)

Parle\\Lexer::build - Завершує набір правил лексера

### Опис

```methodsynopsis
public Parle\Lexer::build(): void
```

Правила, раніше додані за допомогою [Parle\\Lexer::push()](parle-lexer.push.md), завершуються. Цей виклик методу має бути виконано після того, як було застосовано всі необхідні правила. Набір правил доступний лише для читання. Можна розпочинати лексування.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
