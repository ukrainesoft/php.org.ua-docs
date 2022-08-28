Повертає позицію останнього входження підрядка

-   [« iconv\_strpos](function.iconv-strpos.html)
    
-   [iconv\_substr »](function.iconv-substr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции iconv](ref.iconv.html)
    
-   Повертає позицію останнього входження підрядка
    

# iconvstrrpos

(PHP 5, PHP 7, PHP 8)

iconvstrrpos — Повертає позицію останнього входження підрядка

### Опис

```methodsynopsis
iconv_strrpos(string $haystack, string $needle, ?string $encoding = null): int|false
```

Знаходить останню позицію підрядка `needle` у рядку `haystack`

На відміну від [strrpos()](function.strrpos.html) **iconvstrrpos()** повертає зміщення перед рядком у символах, а не в байтах. Кількість символів трактується залежно від вказаної параметром `encoding` кодування.

### Список параметрів

`haystack`

Рядок, в якому проводиться пошук.

`needle`

Шуканий підрядок.

`encoding`

Якщо параметр `encoding` не вказано, то мається на увазі, що `string` має кодування [iconv.internal\_encoding](iconv.configuration.html)

Якщо `haystack` або `needle` не є рядками, вони будуть перетворені на рядок та застосовані як код символу.

### Значення, що повертаються

Повертає номер позиції останнього входження рядка `needle` в `haystack`

Якщо рядок `needle` не знайдена, **iconvstrrpos()** повертає **`false`**

**Увага**

Ця функція може повертати як логічне значення **`false`**так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Описание                                 |
|--------|------------------------------------------|
|        | `encoding` тепер допускає значення null. |

### Дивіться також

-   [strrpos()](function.strrpos.html) - Повертає позицію останнього входження підрядка у рядку
-   [iconv\_strpos()](function.iconv-strpos.html) - Повертає позицію першого входження підрядка
-   [mb\_strrpos()](function.mb-strrpos.html) - Пошук позиції останнього входження одного рядка до іншого