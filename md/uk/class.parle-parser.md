---
navigation:
  - parle-rlexer.reset.md: '« Parle\\RLexer::reset'
  - parle-parser.advance.md: 'Parle\\Parser::advance »'
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас Parle\\Parser
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Parle\\Parser

(PECL parle >= 0.5.1)

## Вступ

Клас парсеру. Правила можна визначати на льоту. Після завершення потрібен екземпляр [Parle\\Lexer](class.parle-lexer.md)для доставки потока токенов.

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
public sigilCount(): int
public sigilName(int $idx): string
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

-   [Parle\\Parser::advance](parle-parser.advance.md) \- Обробляє наступне правило парсера
-   [Parle\\Parser::build](parle-parser.build.md) \- Завершує граматичні правила
-   [Parle\\Parser::consume](parle-parser.consume.md)— Використовує дані для обробки
-   [Parle\\Parser::dump](parle-parser.dump.md) \- Виводить граматику
-   [Parle\\Parser::errorInfo](parle-parser.errorinfo.md)— Отримує інформацію про помилку
-   [Parle\\Parser::left](parle-parser.left.md) \- Оголошує токен з лівою асоціативністю
-   [Parle\\Parser::nonassoc](parle-parser.nonassoc.md) \- Оголошує токен без асоціативності
-   [Parle\\Parser::precedence](parle-parser.precedence.md)— Оголошує правило пріоритету
-   [Parle\\Parser::push](parle-parser.push.md)— Додає граматичне правило
-   [Parle\\Parser::reset](parle-parser.reset.md)— скидає стан парсера
-   [Parle\\Parser::right](parle-parser.right.md)— Оголошує токен із правою асоціативністю
-   [Parle\\Parser::sigil](parle-parser.sigil.md)— Витягує частину збігу за правилом
-   [Parle\\Parser::sigilCount](parle-parser.sigilcount.md)— Отримує кількість елементів у відповідному правилі
-   [Parle\\Parser::sigilName](parle-parser.sigilname.md)— Отримує ім'я правила чи токена
-   [Parle\\Parser::token](parle-parser.token.md) \- Оголошує токен
-   [Parle\\Parser::tokenId](parle-parser.tokenid.md)— Отримує ідентифікатор токена
-   [Parle\\Parser::trace](parle-parser.trace.md)— Слідкує за роботою парсера
-   [Parle\\Parser::validate](parle-parser.validate.md) \- Перевіряє вхідні дані
