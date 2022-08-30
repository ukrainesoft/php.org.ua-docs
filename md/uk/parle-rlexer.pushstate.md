Просуває новий початковий стан

-   [« ParleRLexer::push](parle-rlexer.push.html)
    
-   [ParleRLexer::reset »](parle-rlexer.reset.html)
    
-   [PHP Manual](index.html)
    
-   [ParleRLexer](class.parle-rlexer.html)
    
-   Просуває новий початковий стан
    

# ParleRLexer::pushState

(PECL parle >= 0.5.1)

ParleRLexer::pushState - Просуває новий початковий стан

### Опис

```methodsynopsis
public Parle\RLexer::pushState(string $state): int
```

Цей тип лексера може мати більше одного стану пристрою. Це дозволяє використовувати різні токени залежно від контексту, що дозволяє виконувати простий синтаксичний аналіз. Після відправлення стану його можна використовувати з відповідним варіантом сигнатури [ParleRLexer::push()](parle-rlexer.push.html)

### Список параметрів

`state`

Назва стану

### Значення, що повертаються