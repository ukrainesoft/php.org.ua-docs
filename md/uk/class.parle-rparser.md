Клас ParleRParser

-   [« Parle\\Parser::validate](parle-parser.validate.html)
    
-   [Parle\\RParser::advance »](parle-rparser.advance.html)
    
-   [PHP Manual](index.html)
    
-   [Parle](book.parle.html)
    
-   Клас ParleRParser
    

# Клас ParleRParser

(PECL parle >= 0.7.0)

## Вступ

Клас парсеру. Правила можуть бути визначені на льоту. Після завершення необхідно створити екземпляр [Parle\\RLexer](class.parle-rlexer.html) для доставки потоку токенів.

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

-   [Parle\\RParser::advance](parle-rparser.advance.html) - Обробка наступного правила парсера
-   [Parle\\RParser::build](parle-rparser.build.html) - Завершує граматичні правила
-   [Parle\\RParser::consume](parle-rparser.consume.html) — Використовувати дані для обробки
-   [Parle\\RParser::dump](parle-rparser.dump.html) - Виводить граматику
-   [Parle\\RParser::errorInfo](parle-rparser.errorinfo.html) — Отримує інформацію про помилку
-   [Parle\\RParser::left](parle-rparser.left.html) - Оголошує токен з лівою асоціативністю
-   [Parle\\RParser::nonassoc](parle-rparser.nonassoc.html) - Оголошує токен без асоціативності
-   [Parle\\RParser::precedence](parle-rparser.precedence.html) — Оголошує правило пріоритету
-   [Parle\\RParser::push](parle-rparser.push.html) — Додає граматичне правило
-   [Parle\\RParser::reset](parle-rparser.reset.html) — скидає стан парсера
-   [Parle\\RParser::right](parle-rparser.right.html) — Оголошує токен із правою асоціативністю
-   [Parle\\RParser::sigil](parle-rparser.sigil.html) — Витягує збігаючу частину за правилом
-   [Parle\\RParser::token](parle-rparser.token.html) - Оголошує токен
-   [Parle\\RParser::tokenId](parle-rparser.tokenid.html) — Отримує ідентифікатор токена
-   [Parle\\RParser::trace](parle-rparser.trace.html) — Слідкує за роботою парсера
-   [Parle\\RParser::validate](parle-rparser.validate.html) - Перевіряє вхідні дані