Клас ParleParser

-   [« ParleRLexer::reset](parle-rlexer.reset.html)
    
-   [ParleParser::advance »](parle-parser.advance.html)
    
-   [PHP Manual](index.html)
    
-   [Parle](book.parle.html)
    
-   Клас ParleParser
    

# Клас ParleParser

(PECL parle >= 0.5.1)

## Вступ

Клас парсеру. Правила можна визначати на льоту. Після завершення потрібен екземпляр [ParleLexer](class.parle-lexer.html) для доставки потоку токенів.

## Огляд класів

```classsynopsis



    
     
      class Parle\Parser
     
     {

    /* Константы */
    
     const
     int
      ACTION_ERROR = 0;

    const
     int
      ACTION_SHIFT = 1;

    const
     int
      ACTION_REDUCE = 2;

    const
     int
      ACTION_GOTO = 3;

    const
     int
      ACTION_ACCEPT = 4;

    const
     int
      ERROR_SYNTAX = 0;

    const
     int
      ERROR_NON_ASSOCIATIVE = 1;

    const
     int
      ERROR_UNKNOWN_TOKEN = 2;


    /* Свойства */
    public
     int
      $action = 0;

    public
     int
      $reduceId = 0;


    /* Методы */
    
   public advance(): void
public build(): void
public consume(string $data, Parle\Lexer $lexer): void
public dump(): void
public errorInfo(): Parle\ErrorInfo
public left(string $tok): void
public nonassoc(string $tok): void
public precedence(string $tok): void
public push(string $name, string $rule): int
public reset(int $tokenId = ?): void
public right(string $tok): void
public sigil(int $idx): string
public token(string $tok): void
public tokenId(string $tok): int
public trace(): string
public validate(string $data, Parle\Lexer $lexer): bool

   }
```

## Обумовлені константи

**`Parle\Parser::ACTION_ERROR`**

**`Parle\Parser::ACTION_SHIFT`**

**`Parle\Parser::ACTION_REDUCE`**

**`Parle\Parser::ACTION_GOTO`**

**`Parle\Parser::ACTION_ACCEPT`**

**`Parle\Parser::ERROR_SYNTAX`**

**`Parle\Parser::ERROR_NON_ASSOCIATIVE`**

**`Parle\Parser::ERROR_UNKNOWN_TOKEN`**

## Властивості

action

Поточна дія синтаксичного аналізатора, яка відповідає одній з констант класу дії, тільки для читання.

reduceId

Ідентифікатор правила граматики, щойно оброблений у дії скорочення. Значення відповідає токену чи виробничому ідентифікатору. Лише для читання.

## Зміст

-   [ParleParser::advance](parle-parser.advance.html) - Обробляє наступне правило парсера
-   [ParleParser::build](parle-parser.build.html) - Завершує граматичні правила
-   [ParleParser::consume](parle-parser.consume.html) — Використовує дані для обробки
-   [ParleParser::dump](parle-parser.dump.html) - Виводить граматику
-   [ParleParser::errorInfo](parle-parser.errorinfo.html) — Отримує інформацію про помилку
-   [ParleParser::left](parle-parser.left.html) - Оголошує токен з лівою асоціативністю
-   [ParleParser::nonassoc](parle-parser.nonassoc.html) - Оголошує токен без асоціативності
-   [ParleParser::precedence](parle-parser.precedence.html) — Оголошує правило пріоритету
-   [ParleParser::push](parle-parser.push.html) — Додає граматичне правило
-   [ParleParser::reset](parle-parser.reset.html) — скидає стан парсера
-   [ParleParser::right](parle-parser.right.html) — Оголошує токен із правою асоціативністю
-   [ParleParser::sigil](parle-parser.sigil.html) — Витягує частину збігу за правилом
-   [ParleParser::token](parle-parser.token.html) - Оголошує токен
-   [ParleParser::tokenId](parle-parser.tokenid.html) — Отримує ідентифікатор токена
-   [ParleParser::trace](parle-parser.trace.html) — Слідкує за роботою парсера
-   [ParleParser::validate](parle-parser.validate.html) - Перевіряє вхідні дані