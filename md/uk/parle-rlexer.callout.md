Визначає callback-функцію токена

-   [« Parle\\RLexer::build](parle-rlexer.build.html)
    
-   [Parle\\RLexer::consume »](parle-rlexer.consume.html)
    
-   [PHP Manual](index.html)
    
-   [Parle\\RLexer](class.parle-rlexer.html)
    
-   Визначає callback-функцію токена
    

# ParleRLexer::callout

(PECL parle >= 0.7.2)

ParleRLexer::callout - Визначає callback-функцію токена

### Опис

```methodsynopsis
public Parle\RLexer::callout(int $id, callable $callback): void
```

Визначає callback-функцію, яка буде викликатись, коли лексер зустрічає певний токен.

### Список параметрів

`id`

Token id.

`callback`

Callable-функція. Об'єкт, що викликається, не отримує аргументів, а його значення, що повертається, ігнорується.

### Значення, що повертаються

Функція не повертає значення після виконання.