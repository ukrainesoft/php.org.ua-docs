---
navigation:
  - parle-rlexer.push.md: '« ParleRLexer::push'
  - parle-rlexer.reset.md: 'ParleRLexer::reset »'
  - index.md: PHP Manual
  - class.parle-rlexer.md: ParleRLexer
title: 'ParleRLexer::pushState'
---
# ParleRLexer::pushState

(PECL parle >= 0.5.1)

ParleRLexer::pushState - Просуває новий початковий стан

### Опис

```methodsynopsis
public Parle\RLexer::pushState(string $state): int
```

Цей тип лексера може мати більше одного стану пристрою. Це дозволяє використовувати різні токени залежно від контексту, що дозволяє виконувати простий синтаксичний аналіз. Після відправлення стану його можна використовувати з відповідним варіантом сигнатури [ParleRLexer::push()](parle-rlexer.push.md)

### Список параметрів

`state`

Назва стану

### Значення, що повертаються
