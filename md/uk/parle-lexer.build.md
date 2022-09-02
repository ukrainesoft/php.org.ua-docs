---
navigation:
  - parle-lexer.advance.md: '« ParleLexer::advance'
  - parle-lexer.callout.md: 'ParleLexer::callout »'
  - index.md: PHP Manual
  - class.parle-lexer.md: ParleLexer
title: 'ParleLexer::build'
---
# ParleLexer::build

(PECL parle >= 0.5.1)

ParleLexer::build - Завершує набір правил лексера

### Опис

```methodsynopsis
public Parle\Lexer::build(): void
```

Правила, раніше додані за допомогою [ParleLexer::push()](parle-lexer.push.md), завершуються. Цей виклик методу має бути виконано після того, як було застосовано всі необхідні правила. Набір правил доступний лише для читання. Можна розпочинати лексування.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
