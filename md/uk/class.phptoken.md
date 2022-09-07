---
navigation:
  - tokenizer.examples.md: « Приклади
  - phptoken.construct.md: 'PhpToken::construct »'
  - index.md: PHP Manual
  - book.tokenizer.md: Лексер (Tokenizer)
title: Клас PhpToken
---
# Клас PhpToken

(PHP 8)

## Вступ

Цей клас надає альтернативу функції [tokengetall()](function.token-get-all.md). Тоді як функція повертає токени або у вигляді односимвольного рядка або у вигляді масиву з ідентифікатором токена, його текстом і номером рядка, [PhpToken::tokenize()](phptoken.tokenize.md) нормалізує всі токени в об'єкти PhpToken, що дозволяє набагато зручніше працювати з токенами.

## Огляд класів

```classsynopsis

     
    

    
     
      class PhpToken
     

     implements 
       Stringable {

    /* Свойства */
    
     public
     int
      $id;

    public
     string
      $text;

    public
     int
      $line;

    public
     int
      $pos;


    /* Методы */
    
   final public __construct(    int $id,    string $text,    int $line = -1,    int $pos = -1)

    public getTokenName(): ?string
public is(int|string|array $kind): bool
public isIgnorable(): bool
public __toString(): string
public static tokenize(string $code, int $flags = 0): array

   }
```

## Властивості

ід

Одна з констант T, або символ ASCII представляє односимвольний токен.

text

Текстовий вміст токена.

line

Номер рядка (починаючи з 1), з якого починається токен.

pos

Початкова позиція (починаючи з 0) токена у рядку.

## Зміст

-   [PhpToken::construct](phptoken.construct.md) - Створює об'єкт PhpToken
-   [PhpToken::getTokenName](phptoken.gettokenname.md) - Повертає ім'я токена
-   [PhpToken::is](phptoken.is.md) — Перевіряє, чи відповідає токен зазначеному типу
-   [PhpToken::isIgnorable](phptoken.isignorable.md) — Повідомляє, чи токен ігноруватиметься парсером PHP
-   [PhpToken::toString](phptoken.tostring.md) — Повертає текстовий вміст токена
-   [PhpToken::tokenize](phptoken.tokenize.md) — Розбирає заданий рядок, що містить програму на PHP, масив об'єктів PhpToken
