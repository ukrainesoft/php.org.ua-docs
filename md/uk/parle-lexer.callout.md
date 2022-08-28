Визначає callback-функцію токена

-   [« Parle\\Lexer::build](parle-lexer.build.html)
    
-   [Parle\\Lexer::consume »](parle-lexer.consume.html)
    
-   [PHP Manual](index.html)
    
-   [Parle\\Lexer](class.parle-lexer.html)
    
-   Визначає callback-функцію токена
    

# ParleLexer::callout

(PECL parle >= 0.7.2)

ParleLexer::callout - Визначає callback-функцію токена

### Опис

```methodsynopsis
public Parle\Lexer::callout(int $id, callable $callback): void
```

Визначає callback-функцію, яка буде викликатись, коли лексер зустрічає певний токен.

### Список параметрів

`id`

Ідентифікатор токена.

`callback`

Callable для дзвінка. Об'єкт, що викликається, не отримує аргументів, а його значення, що повертається, ігнорується.

### Значення, що повертаються

Функція не повертає значення після виконання.