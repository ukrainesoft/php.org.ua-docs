---
navigation:
  - parle-rlexer.advance.md: '« Parle\\RLexer::advance'
  - parle-rlexer.callout.md: 'Parle\\RLexer::callout »'
  - index.md: PHP Manual
  - class.parle-rlexer.md: Parle\\RLexer
title: 'Parle\\RLexer::build'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\RLexer::build

(PECL parle >= 0.5.1)

Parle\\RLexer::build - Завершує набір правил лексера

### Опис

```methodsynopsis
public Parle\RLexer::build(): void
```

Правила, раніше додані за допомогою [Parle\\RLexer::push()](parle-rlexer.push.md), завершуються. Виклик методу має бути виконано після того, як усі необхідні правила були передані. Набір правил стає лише читання. Лексер готовий до запуску.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
