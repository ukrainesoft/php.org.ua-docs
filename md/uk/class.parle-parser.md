---
navigation:
  - parle-rlexer.reset.md: '« ParleRLexer::reset'
  - parle-parser.advance.md: 'ParleParser::advance »'
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас ParleParser
---
# Клас ParleParser

(PECL parle >= 0.5.1)

## Вступ

Клас парсеру. Правила можна визначати на льоту. Після завершення потрібен екземпляр [ParleLexer](class.parle-lexer.md) для доставки потоку токенів.

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

-   [ParleParser::advance](parle-parser.advance.md) - Обробляє наступне правило парсера
-   [ParleParser::build](parle-parser.build.md) - Завершує граматичні правила
-   [ParleParser::consume](parle-parser.consume.md) — Використовує дані для обробки
-   [ParleParser::dump](parle-parser.dump.md) - Виводить граматику
-   [ParleParser::errorInfo](parle-parser.errorinfo.md) — Отримує інформацію про помилку
-   [ParleParser::left](parle-parser.left.md) - Оголошує токен з лівою асоціативністю
-   [ParleParser::nonassoc](parle-parser.nonassoc.md) - Оголошує токен без асоціативності
-   [ParleParser::precedence](parle-parser.precedence.md) — Оголошує правило пріоритету
-   [ParleParser::push](parle-parser.push.md) — Додає граматичне правило
-   [ParleParser::reset](parle-parser.reset.md) — скидає стан парсера
-   [ParleParser::right](parle-parser.right.md) — Оголошує токен із правою асоціативністю
-   [ParleParser::sigil](parle-parser.sigil.md) — Витягує частину збігу за правилом
-   [ParleParser::token](parle-parser.token.md) - Оголошує токен
-   [ParleParser::tokenId](parle-parser.tokenid.md) — Отримує ідентифікатор токена
-   [ParleParser::trace](parle-parser.trace.md) — Слідкує за роботою парсера
-   [ParleParser::validate](parle-parser.validate.md) - Перевіряє вхідні дані
