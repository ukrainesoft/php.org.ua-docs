---
navigation:
  - function.ucwords.md: « ucwords
  - function.utf8-encode.md: utf8\_encode »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: utf8\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# utf8\_decode

(PHP 4, PHP 5, PHP 7, PHP 8)

utf8\_decode — Перетворює рядок із кодування UTF-8 на кодування ISO-8859-1, замінюючи неприпустимі або непредставлені символи

**Увага**

Функція оголошена *застарілої* починаючи з PHP 8.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
utf8_decode(string $string): string
```

Функція перетворює рядок `string`из кодировки`UTF-8` у кодування `ISO-8859-1`. Байти у рядку, які не відповідають коректним символам `UTF-8`и символам`UTF-8`, які не існують у `ISO-8859-1` (тобто кодові точки вище `U+00FF`), будуть замінені на символ `?`

> **Зауваження** :
> 
> Багато веб-сторінок, зазначених як кодування `ISO-8859-1`, насправді використовують схоже кодування `Windows-1252`, та веб-браузери інтерпретують сторінки `ISO-8859-1` як `Windows-1252`. Однак `Windows-1252` містить додаткові друковані символи, такі як символ Євро (`€`) та фігурні лапки (`“` `”`) вместо управляющих кодов`ISO-8859-1`. Ця функція не конвертує такі символи `Windows-1252`корректно. Используйте другую функцию, если нужна конвертация в`Windows-1252`

### Список параметрів

`string`

Рядок, закодований в UTF-8.

### Значення, що повертаються

Повертає дані параметра `string`, переведені на кодування ISO-8859-1.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функцію оголошено застарілою. |
| 7.2.0 | Функцію було перенесено з модуля XML в ядро ​​PHP. У попередніх версіях вона була доступна лише за встановленого модуля XML. |

### Приклади

**Приклад #1 Простий приклад**

```php
<?php
// Преобразование строки 'Zoë' из UTF-8 в ISO 8859-1
$utf8_string = "\x5A\x6F\xC3\xAB";
$iso8859_1_string = utf8_decode($utf8_string);
echo bin2hex($iso8859_1_string), "\n";

// Неправильные последовательности UTF-8 заменяются на '?'
$invalid_utf8_string = "\xC3";
$iso8859_1_string = utf8_decode($invalid_utf8_string);
var_dump($iso8859_1_string);

// Символы, не существующие в ISO 8859-1, такие как
// '€' (Знак евро) также заменяются на '?'
$utf8_string = "\xE2\x82\xAC";
$iso8859_1_string = utf8_decode($utf8_string);
var_dump($iso8859_1_string);
?>
```

Результат виконання наведеного прикладу:

```
5a6feb
string(1) "?"
string(1) "?"
```

### Примітки

> **Зауваження** **Застаріння та альтернативи**
> 
> Функция*застаріла*починаючи з PHP 8.2.0 і буде видалена в майбутній версії. Існуючі варіанти використання повинні бути перевірені та замінені відповідними альтернативами.
> 
> Аналогічної функціональності можна досягти за допомогою функції [mb\_convert\_encoding()](function.mb-convert-encoding.md), яка підтримує ISO-8859-1 та багато інших кодування символів.
> 
> ```php
> <?php
> $utf8_string = "\xC3\xAB"; // 'ë' (e з дієрезисом) у UTF-8
> $iso8859_1_string = mb_convert_encoding($utf8_string, 'ISO-8859-1', 'UTF-8');
> echo bin2hex($iso8859_1_string), "\n";
> 
> $utf8_string = "\xCE\xBB"; // 'λ' (Грецька рядкова лямбда) в UTF-8
> $iso8859_7_string = mb_convert_encoding($utf8_string, 'ISO-8859-7', 'UTF-8');
> echo bin2hex($iso8859_7_string), "\n";
> 
> $utf8_string = "\xE2\x82\xAC"; // '€' (Символ євро) в UTF-8 (відсутнє в ISO-8859-1)
> $windows_1252_string = mb_convert_encoding($utf8_string, 'Windows-1252', 'UTF-8');
> echo bin2hex($windows_1252_string), "\n";
> ?>
> ```
> 
> Результат виконання наведеного прикладу:
> 
> ```
> eb
> eb
> 80
> ```
> 
> Інші опції, які можуть бути доступні в залежності від встановлених модулів: [UConverter::transcode()](uconverter.transcode.md) і [iconv()](function.iconv.md)
> 
> Всі наступні варіанти дають той самий результат:
> 
> ```php
> <?php
> $utf8_string = "x5Ax6FxC3xAB"; // 'Zoë' в UTF-8
> $iso8859_1_string = utf8_decode($utf8_string);
> echo bin2hex($iso8859_1_string), "\n";
> 
> $iso8859_1_string = mb_convert_encoding($utf8_string, 'ISO-8859-1', 'UTF-8');
> echo bin2hex($iso8859_1_string), "\n";
> 
> $iso8859_1_string = iconv('UTF-8', 'ISO-8859-1', $utf8_string);
> echo bin2hex($iso8859_1_string), "\n";
> 
> $iso8859_1_string = UConverter::transcode($utf8_string, 'ISO-8859-1', 'UTF8');
> echo bin2hex($iso8859_1_string), "\n";
> ?>
> ```
> 
> Результат виконання наведеного прикладу:
> 
> ```
> 5a6feb
> 5a6feb
> 5a6feb
> 5a6feb
> ```
> 
> Указание`'?'` як опція `'to_subst'`в методе[UConverter::transcode()](uconverter.transcode.md) дає той самий результат, що і функція **utf8\_decode()** для рядків, які є неприпустимими або не можуть бути подані ISO 8859-1.
> 
> ```php
> <?php
> $utf8_string = "\xE2\x82\xAC"; // € (Символ євро) відсутня у ISO-8859-1
> $iso8859_1_string = UConverter::transcode(
>     $utf8_string, 'ISO-8859-1', 'UTF-8', ['to_subst' => '?']
> );
> var_dump($iso8859_1_string);
> ?>
> ```
> 
> Результат виконання наведеного прикладу:
> 
> ```
> sring(1) "?"
> ```

### Дивіться також

-   [utf8\_encode()](function.utf8-encode.md) \- Перетворює рядок із ISO-8859-1 на UTF-8
-   [mb\_convert\_encoding()](function.mb-convert-encoding.md) \- Перетворює рядок з одного кодування символів на інший
-   [UConverter::transcode()](uconverter.transcode.md) \- Перетворює рядок з одного кодування символів на інший
-   [iconv()](function.iconv.md) \- Перетворює рядок з одного кодування символів на інший
