Клас PhpToken

-   [« Приклади](tokenizer.examples.html)
    
-   [PhpToken::construct »](phptoken.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Лексер (Tokenizer)](book.tokenizer.html)
    
-   Клас PhpToken
    

# Клас PhpToken

(PHP 8)

## Вступ

Цей клас надає альтернативу функції [tokengetall()](function.token-get-all.html). Тоді як функція повертає токени або у вигляді односимвольного рядка або у вигляді масиву з ідентифікатором токена, його текстом і номером рядка, [PhpToken::tokenize()](phptoken.tokenize.html) нормалізує всі токени в об'єкти PhpToken, що дозволяє набагато зручніше працювати з токенами.

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
    
   final public __construct(    int $id,    string $text,    int $line = -1,    int $pos = -1)

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

-   [PhpToken::construct](phptoken.construct.html) - Створює об'єкт PhpToken
-   [PhpToken::getTokenName](phptoken.gettokenname.html) - Повертає ім'я токена
-   [PhpToken::is](phptoken.is.html) — Перевіряє, чи відповідає токен зазначеному типу
-   [PhpToken::isIgnorable](phptoken.isignorable.html) — Повідомляє, чи токен ігноруватиметься парсером PHP
-   [PhpToken::toString](phptoken.tostring.html) — Повертає текстовий вміст токена
-   [PhpToken::tokenize](phptoken.tokenize.html) — Розбирає заданий рядок, що містить програму на PHP, масив об'єктів PhpToken