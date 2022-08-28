Клас ParleLexer

-   [« Пример использования парсера](parle.examples.parser.html)
    
-   [Parle\\Lexer::advance »](parle-lexer.advance.html)
    
-   [PHP Manual](index.html)
    
-   [Parle](book.parle.html)
    
-   Клас ParleLexer
    

# Клас ParleLexer

(PECL parle >= 0.5.1)

## Вступ

Клас лексера з одним станом. Лексеми можна визначати на льоту. Якщо конкретний екземпляр лексера призначений для використання з [Parle\\Parser](class.parle-parser.html)Ідентифікатори токенів повинні бути взяті звідти. В іншому випадку можуть бути надані довільні ідентифікатори токенів. Лексер може дати певну перевагу у продуктивності в порівнянні з [Parle\\RLexer](class.parle-rlexer.html)якщо не потрібно кілька станів. Зверніть увагу, що [Parle\\RParser](class.parle-rparser.html) несумісний із цим лексером.

## Огляд класів

```classsynopsis



    
     
      class Parle\Lexer
     
     {

    /* Константы */
    
     const
     int
      ICASE = 1;

    const
     int
      DOT_NOT_LF = 2;

    const
     int
      DOT_NOT_CRLF = 4;

    const
     int
      SKIP_WS = 8;

    const
     int
      MATCH_ZERO_LEN = 16;


    /* Свойства */
    public
     bool
      $bol = false;

    public
     int
      $flags = 0;

    public
     int
      $state = 0;

    public
     int
      $marker = 0;

    public
     int
      $cursor = 0;


    /* Методы */
    
   public advance(): void
public build(): void
public callout(int $id, callable $callback): void
public consume(string $data): void
public dump(): void
public getToken(): Parle\Token
public insertMacro(string $name, string $regex): void
public push(string $regex, int $id): void
public reset(int $pos): void

   }
```

## Обумовлені константи

**`Parle\Lexer::ICASE`**

**`Parle\Lexer::DOT_NOT_LF`**

**`Parle\Lexer::DOT_NOT_CRLF`**

**`Parle\Lexer::SKIP_WS`**

**`Parle\Lexer::MATCH_ZERO_LEN`**

## Властивості

біль

Прапор початку введення.

flags

Прапори лексера.

state

Поточний стан лексера доступний тільки для читання.

marker

Позиція останнього збігу токена доступна тільки для читання.

cursor

Поточне зміщення введення доступне тільки для читання.

## Зміст

-   [Parle\\Lexer::advance](parle-lexer.advance.html) - Обробляє таке правило лексера
-   [Parle\\Lexer::build](parle-lexer.build.html) - Завершує набір правил лексера
-   [Parle\\Lexer::callout](parle-lexer.callout.html) - Визначає callback-функцію токена
-   [Parle\\Lexer::consume](parle-lexer.consume.html) - Передає дані на обробку
-   [Parle\\Lexer::dump](parle-lexer.dump.html) - Виводить стан пристрою
-   [Parle\\Lexer::getToken](parle-lexer.gettoken.html) — Отримує поточний токен
-   [Parle\\Lexer::insertMacro](parle-lexer.insertmacro.html) — Вставляє макрос регулярного виразу
-   [Parle\\Lexer::push](parle-lexer.push.html) - Додає правило лексера
-   [Parle\\Lexer::reset](parle-lexer.reset.html) - скидає лексер