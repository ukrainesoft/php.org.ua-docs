Додає правило лексера

-   [« Parle\\Lexer::insertMacro](parle-lexer.insertmacro.html)
    
-   [Parle\\Lexer::reset »](parle-lexer.reset.html)
    
-   [PHP Manual](index.html)
    
-   [Parle\\Lexer](class.parle-lexer.html)
    
-   Додає правило лексера
    

# ParleLexer::push

(PECL parle >= 0.5.1)

ParleLexer::push - Додає правило лексера

### Опис

```methodsynopsis
public Parle\Lexer::push(string $regex, int $id): void
```

Висуває шаблон для розпізнавання лексеми.

### Список параметрів

`regex`

Регулярне вираз, використовуване зіставлення токенів.

`id`

Ідентифікатор токена. Якщо екземпляр лексера призначений для автономного використання, то може бути довільним числом. Якщо екземпляр лексера буде переданий синтаксичному аналізатору, має бути ідентифікатор, який повертається [Parle\\Parser::tokenid()](parle-parser.tokenid.html)

### Значення, що повертаються

Функція не повертає значення після виконання.