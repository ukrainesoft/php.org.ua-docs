---
navigation:
  - parle-rlexer.advance.md: '« ParleRLexer::advance'
  - parle-rlexer.callout.md: 'ParleRLexer::callout »'
  - index.md: PHP Manual
  - class.parle-rlexer.md: ParleRLexer
title: 'ParleRLexer::build'
---
# ParleRLexer::build

(PECL parle >= 0.5.1)

ParleRLexer::build - Завершує набір правил лексера

### Опис

```methodsynopsis
public Parle\RLexer::build(): void
```

Правила, раніше додані за допомогою [ParleRLexer::push()](parle-rlexer.push.md), завершуються. Виклик методу має бути виконаний після того, як усі необхідні правила були передані. Набір правил стає лише читання. Лексер готовий до запуску.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
