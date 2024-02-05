---
navigation:
  - parle-rlexer.push.md: '« Parle\\RLexer::push'
  - parle-rlexer.reset.md: 'Parle\\RLexer::reset »'
  - index.md: PHP Manual
  - class.parle-rlexer.md: Parle\\RLexer
title: 'Parle\\RLexer::pushState'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Parle\\RLexer::pushState

(PECL parle >= 0.5.1)

Parle\\RLexer::pushState - Просуває новий початковий стан

### Опис

```methodsynopsis
public Parle\RLexer::pushState(string $state): int
```

Цей тип лексера може мати більше одного стану пристрою. Це дозволяє використовувати різні токени залежно від контексту, що дозволяє виконувати простий синтаксичний аналіз. Після відправлення стану його можна використовувати з відповідним варіантом сигнатури [Parle\\RLexer::push()](parle-rlexer.push.md)

### Список параметрів

`state`

Назва стану

### Значення, що повертаються
