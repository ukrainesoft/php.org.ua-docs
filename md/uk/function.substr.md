Повертає підрядок

-   [« substr\_replace](function.substr-replace.html)
    
-   [trim »](function.trim.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Повертає підрядок
    

# substr

(PHP 4, PHP 5, PHP 7, PHP 8)

substr — Повертає підрядок

### Опис

```methodsynopsis
substr(string $string, int $offset, ?int $length = null): string
```

Повертає рядок рядка `string`, що починається з `offset` символу за рахунком та довжиною `length` символів.

### Список параметрів

`string`

Вхідний рядок.

`offset`

Якщо `offset` невід'ємний, підрядок, що повертається, починається з позиції `offset` від початку рядка, рахуючи від нуля. Наприклад, у рядку '`abcdef`', у позиції `0` знаходиться символ '`a`', у позиції `2` - символ '`c`', і т.д.

Якщо `offset` негативний, повертається підрядок починається з позиції, що віддаляється на `offset` символів від кінця рядка `string`

Якщо `string` менше `offset` символів буде повернено порожній рядок.

**Приклад #1 Використання негативного параметра `offset`**

```php
<?php
$rest = substr("abcdef", -1);    // возвращает "f"
$rest = substr("abcdef", -2);    // возвращает "ef"
$rest = substr("abcdef", -3, 1); // возвращает "d"
?>
```

`length`

Якщо `length` позитивний рядок, що повертається, буде не довшим `length` символів, починаючи з параметра `offset` (залежно від довжини `string`

Якщо `length` негативний, то буде відкинуто зазначене цим аргументом кількість символів з кінця рядка `string` (після того як буде обчислено стартову позицію, якщо `offset` негативний). Якщо при цьому позиція почала підрядки, яка визначається аргументом `offset`, знаходиться у відкинутій частині рядка або за нею, повертається порожній рядок.

Якщо параметр `length` заданий і рівний `0`, буде повернено порожній рядок.

Якщо параметр `length` опущений або **`null`**, то буде повернуто підрядок, що починається з позиції, вказаної параметром `offset` і рядка, що триває до кінця.

**Приклад #2 Використання негативного параметра `length`**

```php
<?php
$rest = substr("abcdef", 0, -1);  // возвращает "abcde"
$rest = substr("abcdef", 2, -1);  // возвращает "cde"
$rest = substr("abcdef", 4, -4);  // возвращает ""; до PHP 8.0.0 возвращалось false
$rest = substr("abcdef", -3, -1); // возвращает "de"
?>
```

### Значення, що повертаються

Повертає вилучену частину параметра `string` або порожній рядок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `length` тепер допускає значення null. Якщо значення параметра `length` явно поставлено як **`null`**, функція повертає підрядок, що закінчується в кінці рядка; раніше повертався порожній рядок. |
|  | Функція повертає порожній рядок там, де раніше повертала **`false`** |

### Приклади

**Приклад #3 Базове використання **substr()****

```php
<?php
echo substr('abcdef', 1);     // bcdef
echo substr("abcdef", 1, null); // bcdef; до PHP 8.0.0 возвращалась пустая строка
echo substr('abcdef', 1, 3);  // bcd
echo substr('abcdef', 0, 4);  // abcd
echo substr('abcdef', 0, 8);  // abcdef
echo substr('abcdef', -1, 1); // f

// Получить доступ к отдельному символу в строке
// можно также с помощью квадратных скобок
$string = 'abcdef';
echo $string[0];                 // a
echo $string[3];                 // d
echo $string[strlen($string)-1]; // f

?>
```

**Приклад #4 **substr()** та приведення типів**

```php
<?php
class apple {
    public function __toString() {
        return "green";
    }
}

echo "1) ".var_export(substr("pear", 0, 2), true).PHP_EOL;
echo "2) ".var_export(substr(54321, 0, 2), true).PHP_EOL;
echo "3) ".var_export(substr(new apple(), 0, 2), true).PHP_EOL;
echo "4) ".var_export(substr(true, 0, 1), true).PHP_EOL;
echo "5) ".var_export(substr(false, 0, 1), true).PHP_EOL;
echo "6) ".var_export(substr("", 0, 1), true).PHP_EOL;
echo "7) ".var_export(substr(1.2e3, 0, 4), true).PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
1) 'pe'
2) '54'
3) 'gr'
4) '1'
5) ''
6) ''
7) '1200'
```

**Приклад #5 Неприпустимий діапазон символів**

Якщо запитується неприпустимий діапазон символів, **substr()** повертає порожній рядок, починаючи з PHP 8.0.0; раніше поверталося **`false`**

```php
<?php
var_dump(substr('a', 2));
?>
```

Результат виконання цього прикладу в PHP 8:

```
string(0) ""
```

Результат виконання цього прикладу в PHP 7:

```
bool(false)
```

### Дивіться також

-   [strrchr()](function.strrchr.html) - Знаходить останнє входження символу у рядку
-   [substr\_replace()](function.substr-replace.html) - Замінює частину рядка
-   [preg\_match()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [trim()](function.trim.html) - Видаляє прогалини (або інші символи) з початку та кінця рядка
-   [mb\_substr()](function.mb-substr.html) - Повертає частину рядка
-   [wordwrap()](function.wordwrap.html) - Переносить рядок за вказаною кількістю символів
-   [Посимвольный доступ и изменение строки](language.types.string.html#language.types.string.substr)