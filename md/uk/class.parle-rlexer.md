---
navigation:
  - parle-lexer.reset.html: '« ParleLexer::reset'
  - parle-rlexer.advance.html: 'ParleRLexer::advance »'
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас ParleRLexer
---
# Клас ParleRLexer

(PECL parle >= 0.5.1)

## Вступ

Клас лексера з кількома станами. Лексеми можна визначати на льоту. Якщо конкретний екземпляр лексера призначений для використання з [ParleRParser](class.parle-rparser.html)Ідентифікатори токенів повинні бути взяті звідти. В іншому випадку можуть бути надані довільні ідентифікатори токенів. Зверніть увагу, що [ParleParser](class.parle-parser.md) несумісний із цим лексером.

## Огляд класів

```classsynopsis



    
     
      class Parle\RLexer
     
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
public push(    string $state,    string $regex,    int $id,    string $newState): void
public push(string $state, string $regex, string $newState): void
public pushState(string $state): int
public reset(int $pos): void

   }
```

## Обумовлені константи

**`Parle\RLexer::ICASE`**

**`Parle\RLexer::DOT_NOT_LF`**

**`Parle\RLexer::DOT_NOT_CRLF`**

**`Parle\RLexer::SKIP_WS`**

**`Parle\RLexer::MATCH_ZERO_LEN`**

## Властивості

біль

Прапор початку введення.

flags

Прапори лексера.

state

Поточний стан лексера, лише читання.

marker

Позиція останнього збігу токена, лише читання.

cursor

Поточне усунення введення, тільки для читання.

## Зміст

-   [ParleRLexer::advance](parle-rlexer.advance.md) - Обробка наступного правила лексера
-   [ParleRLexer::build](parle-rlexer.build.md) - Завершує набір правил лексера
-   [ParleRLexer::callout](parle-rlexer.callout.md) - Визначає callback-функцію токена
-   [ParleRLexer::consume](parle-rlexer.consume.md) — Передає дані для обробки
-   [ParleRLexer::dump](parle-rlexer.dump.md) — Вивантажує стан пристрою
-   [ParleRLexer::getToken](parle-rlexer.gettoken.md) - в
-   [ParleRLexer::insertMacro](parle-rlexer.insertmacro.md) — Вставляє макрос регулярного виразу
-   [ParleRLexer::push](parle-rlexer.push.md) - Додає правило лексера
-   [ParleRLexer::pushState](parle-rlexer.pushstate.md) - Просуває новий початковий стан
-   [ParleRLexer::reset](parle-rlexer.reset.md) - скидає лексер
