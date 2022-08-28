Таблиця порівняння типів у PHP

-   [« Unix-сокеты: UNIX и UDG](transports.unix.html)
    
-   [Список меток (tokens) парсера »](tokens.html)
    
-   [PHP Manual](index.html)
    
-   [Appendices](appendices.html)
    
-   Таблиця порівняння типів у PHP
    

# Таблиця порівняння типів у PHP

Наступні таблиці демонструють роботу PHP з [типами переменных](language.types.html) і [операторами сравнения](language.operators.comparison.html), як у разі вільного, і у разі суворого порівняння. Також ця інформація відноситься до розділу документації з [приведению типов](language.types.type-juggling.html). Натхненням на створення цього розділу ми зобов'язані різним коментарям користувачів та роботі над [» BlueShoes](http://www.blueshoes.org/en/developer/php_cheat_sheet/)

До огляду таблиць важливо знати і розуміти типи змінних та їх значення. Наприклад, `"42"` - string, у той час як `42` - int . **`false`** - bool, а `"false"` - string.

> **Зауваження**
> 
> HTML-форми не передають цілі, дробові чи булеві змінні: вони завжди передають рядки. Для перевірки чи рядок числом, використовуйте функцію [is\_numeric()](function.is-numeric.html)

> **Зауваження**
> 
> Використання `if ($x)`якщо $x не визначена, згенерує помилку рівня **`E_NOTICE`**. Натомість використовуйте функцію [empty()](function.empty.html) або [isset()](function.isset.html) та/або ініціалізуйте змінну.

> **Зауваження**
> 
> Деякі арифметичні операції можуть повернути значення, надане константою **`NAN`** (Not A Number, не-число). Будь-яке суворе чи не суворе порівняння цього значення з будь-яким іншим, включаючи його самого, але виключаючи **`true`**, поверне **`false`** (тобто . `NAN != NAN` і `NAN !== NAN`). Прикладами операцій, що повертають **`NAN`**, є `sqrt(-1)` `asin(2)` і `acosh(0)`

**Порівняння типів $x та результатів функцій PHP, пов'язаних з типами**

| Выражение          | [gettype()](function.gettype.html) | [empty()](function.empty.html) | [is\_null()](function.is-null.html) | [isset()](function.isset.html) | bool : `if($x)` |
|--------------------|------------------------------------|--------------------------------|-------------------------------------|--------------------------------|-----------------|
| `$x = "";`         | string                             | **`true`**                     | **`false`**                         | **`true`**                     | **`false`**     |
| `$x = null;`       | NULL                               | **`true`**                     | **`true`**                          | **`false`**                    | **`false`**     |
| `var $x;`          | NULL                               | **`true`**                     | **`true`**                          | **`false`**                    | **`false`**     |
| $x не визначено    | NULL                               | **`true`**                     | **`true`**                          | **`false`**                    | **`false`**     |
| `$x = [];`         | array                              | **`true`**                     | **`false`**                         | **`true`**                     | **`false`**     |
| `$x = ['a', 'b'];` | array                              | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = false;`      | bool                               | **`true`**                     | **`false`**                         | **`true`**                     | **`false`**     |
| `$x = true;`       | bool                               | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = 1;`          | int                                | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = 42;`         | int                                | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = 0;`          | int                                | **`true`**                     | **`false`**                         | **`true`**                     | **`false`**     |
| `$x = -1;`         | int                                | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = "1";`        | string                             | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = "0";`        | string                             | **`true`**                     | **`false`**                         | **`true`**                     | **`false`**     |
| `$x = "-1";`       | string                             | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = "php";`      | string                             | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = "true";`     | string                             | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |
| `$x = "false";`    | string                             | **`false`**                    | **`false`**                         | **`true`**                     | **`true`**      |

**Гнучке порівняння за допомогою `==`**

|             | **`true`**  | **`false`** | `1`         | `0`         | `-1`        | `"1"`       | `"0"`       | `"-1"`      | **`null`**  | `[]`        | `"php"`     | `""`        |
|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **`true`**  | **`true`**  | **`false`** | **`true`**  | **`false`** | **`true`**  | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** |
| **`false`** | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`true`**  | **`true`**  | **`false`** | **`true`**  |
| `1`         | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `0`         | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** |
| `-1`        | **`true`**  | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** |
| `"1"`       | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"0"`       | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"-1"`      | **`true`**  | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** |
| **`null`**  | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`true`**  | **`false`** | **`true`**  |
| `[]`        | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`true`**  | **`false`** | **`false`** |
| `"php"`     | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** |
| `""`        | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  |

**`true`** до PHP 8.0.0.

**Жорстке порівняння за допомогою `===`**

|             | **`true`**  | **`false`** | `1`         | `0`         | `-1`        | `"1"`       | `"0"`       | `"-1"`      | **`null`**  | `[]`        | `"php"`     | `""`        |
|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **`true`**  | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `1`         | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `0`         | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `-1`        | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"1"`       | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"0"`       | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| `"-1"`      | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** |
| **`null`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** |
| `[]`        | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** |
| `"php"`     | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** |
| `""`        | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  |