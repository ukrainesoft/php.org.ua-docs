---
navigation:
  - uconverter.toucallback.md: '« UConverter::toUCallback'
  - ref.intl.grapheme.md: Функції Grapheme »
  - index.md: PHP Manual
  - class.uconverter.md: UConverter
title: 'UConverter::transcode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UConverter::transcode

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

UConverter::transcode — Перетворює рядок з одного кодування символів на інший

### Опис

```methodsynopsis
public static UConverter::transcode(    string $str,    string $toEncoding,    string $fromEncoding,    ?array $options = null): string|false
```

Перетворює рядок `str`из кодировки`fromEncoding`в`toEncoding`

### Список параметрів

`str`

Рядок (string) для перетворення.

`toEncoding`

Необхідне кодування результату.

`fromEncoding`

Поточне кодування рядка `str`

`options`

Необов'язковий масив (array), який може містити такі ключі:

-   `'to_subst'`\- підстановочний символ, який використовується замість будь-якого символу рядка`str`, який не може бути закодований у`toEncoding`. Якщо ключ вказано, він повинен представляти один символ у цільовому кодуванні.

### Значення, що повертаються

Возвращает преобразованную строку или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Перетворення з UTF-8 на UTF-16 і назад**

```php
<?php
$utf8_string = "\x5A\x6F\xC3\xAB"; // 'Zoë' в UTF-8
$utf16_string = UConverter::transcode($utf8_string, 'UTF-16BE', 'UTF-8');
echo bin2hex($utf16_string), "\n";

$new_utf8_string = UConverter::transcode($utf16_string, 'UTF-8', 'UTF-16BE');
echo bin2hex($new_utf8_string), "\n";
?>
```

Результат виконання наведеного прикладу:

```
005a006f00eb
5a6fc3ab
```

**Приклад #2 Неприпустимі символи у вхідному рядку**

Якщо вхідний рядок містить послідовність байтів, яка не є допустимою у кодуванні, зазначеній у `fromEncoding`, то перед преобразованием в`toEncoding`она заменяется кодовой точкой Unicode U+FFFD (Заменяющий символ).

```php
<?php
$invalid_utf8_string = "\xC3"; // неполная многобайтовая последовательность UTF-8
$utf16_string = UConverter::transcode($invalid_utf8_string, 'UTF-16BE', 'UTF-8');
echo bin2hex($utf16_string), "\n";
?>
```

Результат виконання наведеного прикладу:

```
fffd
```

**Приклад #3 Символи, які не можуть бути закодовані**

Якщо вхідний рядок містить символи, які не можуть бути представлені у кодуванні `toEncoding`, вони замінюються одним символом. За замовчуванням символ залежить від кодування і може керуватися за допомогою параметра `'to_subst'`

```php
<?php
$utf8_string = "\xE2\x82\xAC"; // € (Знак евро) не существует в ISO 8859-1

// Замена по умолчанию в ISO 8859-1 - "\x1A" (Заменитель)
$iso8859_1_string = UConverter::transcode($utf8_string, 'ISO-8859-1', 'UTF-8');
echo bin2hex($iso8859_1_string), "\n";

// Использование в качестве заменителя символа '?' ("\x3F").
$iso8859_1_string = UConverter::transcode(
    $utf8_string, 'ISO-8859-1', 'UTF-8', ['to_subst' => '?']
);
echo bin2hex($iso8859_1_string), "\n";

// Поскольку ISO 8859-1 не может отобразить U+FFFD, недействительная входная строка также заменяется на to_subst
$invalid_utf8_string = "\xC3"; // неполная многобайтовая последовательность UTF-8
$iso8859_1_string = UConverter::transcode(
    $invalid_utf8_string, 'ISO-8859-1', 'UTF-8', ['to_subst' => '?']
);
echo bin2hex($iso8859_1_string), "\n";
?>
```

Результат виконання наведеного прикладу:

```
1a
3f
3f
```

### Дивіться також

-   [mb\_convert\_encoding()](function.mb-convert-encoding.md) \- Перетворює рядок з одного кодування символів на інший
-   [iconv()](function.iconv.md) \- Перетворює рядок з одного кодування символів на інший
