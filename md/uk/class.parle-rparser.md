---
navigation:
  - parle-parser.validate.html: '« ParleParser::validate'
  - parle-rparser.advance.html: 'ParleRParser::advance »'
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас ParleRParser
---
# Клас ParleRParser

(PECL parle >= 0.7.0)

## Вступ

Клас парсеру. Правила можуть бути визначені на льоту. Після завершення необхідно створити екземпляр [ParleRLexer](class.parle-rlexer.md) для доставки потоку токенів.

## Огляд класів

```classsynopsis



    
     
      class Parle\RParser
     
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
public consume(string $data, Parle\RLexer $rlexer): void
public dump(): void
public errorInfo(): Parle\ErrorInfo
public left(string $tok): void
public nonassoc(string $tok): void
public precedence(string $tok): void
public push(string $name, string $rule): int
public reset(int $tokenId = ?): void
public right(string $tok): void
public sigil(int $idx = ?): string
public token(string $tok): void
public tokenId(string $tok): int
public trace(): string
public validate(string $data, Parle\RLexer $lexer): bool

   }
```

## Обумовлені константи

**`Parle\RParser::ACTION_ERROR`**

**`Parle\RParser::ACTION_SHIFT`**

**`Parle\RParser::ACTION_REDUCE`**

**`Parle\RParser::ACTION_GOTO`**

**`Parle\RParser::ACTION_ACCEPT`**

**`Parle\RParser::ERROR_SYNTAX`**

**`Parle\RParser::ERROR_NON_ASSOCIATIVE`**

**`Parle\RParser::ERROR_UNKNOWN_TOKEN`**

## Властивості

action

Поточна дія парсера, яка відповідає одній із констант класу дії, лише для читання.

reduceId

Ідентифікатор правила граматики, щойно оброблений у дії скорочення. Значення відповідає токену чи виробничому ідентифікатору. Лише для читання.

## Зміст

-   [ParleRParser::advance](parle-rparser.advance.md) - Обробка наступного правила парсера
-   [ParleRParser::build](parle-rparser.build.md) - Завершує граматичні правила
-   [ParleRParser::consume](parle-rparser.consume.md) — Використовувати дані для обробки
-   [ParleRParser::dump](parle-rparser.dump.md) - Виводить граматику
-   [ParleRParser::errorInfo](parle-rparser.errorinfo.md) — Отримує інформацію про помилку
-   [ParleRParser::left](parle-rparser.left.md) - Оголошує токен з лівою асоціативністю
-   [ParleRParser::nonassoc](parle-rparser.nonassoc.md) - Оголошує токен без асоціативності
-   [ParleRParser::precedence](parle-rparser.precedence.md) — Оголошує правило пріоритету
-   [ParleRParser::push](parle-rparser.push.md) — Додає граматичне правило
-   [ParleRParser::reset](parle-rparser.reset.md) — скидає стан парсера
-   [ParleRParser::right](parle-rparser.right.md) — Оголошує токен із правою асоціативністю
-   [ParleRParser::sigil](parle-rparser.sigil.md) — Витягує збігаючу частину за правилом
-   [ParleRParser::token](parle-rparser.token.md) - Оголошує токен
-   [ParleRParser::tokenId](parle-rparser.tokenid.md) — Отримує ідентифікатор токена
-   [ParleRParser::trace](parle-rparser.trace.md) — Слідкує за роботою парсера
-   [ParleRParser::validate](parle-rparser.validate.md) - Перевіряє вхідні дані
