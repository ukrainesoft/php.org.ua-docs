---
navigation:
  - function.urldecode.md: « urldecode
  - book.v8js.md: V8js »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: urlencode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# urlencode

(PHP 4, PHP 5, PHP 7, PHP 8)

urlencode — URL-кодування рядка

### Опис

```methodsynopsis
urlencode(string $string): string
```

Ця функція зручна, коли кодований рядок буде використовуватися в запиті, як частина URL, як зручний спосіб передачі змінних на наступну сторінку.

### Список параметрів

`string`

Рядок, який має бути закодований.

### Значення, що повертаються

Повертає рядок, в якому всі не цифро-літерні символи, крім `-_.` повинні бути замінені знаком відсотка (`%`), за яким слідує два шістнадцяткових числа, а пробіли закодовані як знак додавання (`+` ). Рядок кодується тим же способом, що й POST-дані веб-форми, тобто за типом контенту `application/x-www-form-urlencoded`. Це відрізняється від кодування по [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)(смотрите[rawurlencode()](function.rawurlencode.md) ) в тому, що з історичних причин пробіли кодуються як знак "плюс" (+).

### Приклади

**Приклад #1 Приклад використання** urlencode()\*\*\*\*

```php
<?php
$userinput = 'Data123!@-_ +';
echo "Пользовательские данные: $userinput\n";
echo '<a href="mycgi?foo=', urlencode($userinput), '">';
?>
```

Результат виконання наведеного прикладу:

```
Пользовательские данные: Data123!@-_ +
<a href="mycgi?foo=Data123%21%40-_+%2B">
```

**Приклад #2 Приклад використання** urlencode()**и[htmlentities()](function.mdentities.md)**

```php
<?php
$foo = 'Data123!@-_ +';
$bar = "Содержимое, отличное от $foo";
echo "foo: $foo\n";
echo "bar: $bar\n";
$query_string = 'foo=' . urlencode($foo) . '&bar=' . urlencode($bar);
echo '<a href="mycgi?' . htmlentities($query_string) . '">';
?>
```

Результат виконання наведеного прикладу:

```
foo: Data123!@-_ +
bar: Содержимое, отличное от Data123!@-_ +
<a href="mycgi?foo=Data123%21%40-_+%2B&amp;bar=Not+the+same+content+as+Data123%21%40-_+%2B">
```

### Примітки

> **Зауваження** :
> 
> Будьте уважні зі змінними, які можуть збігатися з елементами HTML. Такі сутності як &, © та £ розбираються браузером і використовується як реальна сутність, а не бажане ім'я змінної. Це очевидний конфлікт, який W3C вказує протягом багатьох років. Дивіться подробиці: [» http://www.w3.org/TR/html4/appendix/notes.md#h-B.2.2](http://www.w3.org/TR/html4/appendix/notes.md#h-B.2.2)
> 
> PHP підтримує зміну роздільника аргументів на рекомендований W3C символ "точку з комою" шляхом зміни директиви arg\_separator у файлі .ini. На жаль, більшість додатків користувача не відправляють дані форми у форматі з роздільником "точка з комою". Більше переносимий спосіб вирішити цю проблему - це використовувати & замість & як роздільник. Вам не потрібно буде для цього змінювати PHP-директиву arg\_separator. Залишіть розділювач як &, але кодуйте ваші URL-адреси за допомогою [htmlentities()](function.mdentities.md) або [htmlspecialchars()](function.mdspecialchars.md)

### Дивіться також

-   [urldecode()](function.urldecode.md) \- Декодування URL-кодованого рядка
-   [htmlentities()](function.mdentities.md) \- Перетворює всі можливі символи у відповідні HTML-сутності
-   [rawurlencode()](function.rawurlencode.md) \- URL-кодування рядка згідно з RFC 3986
-   [rawurldecode()](function.rawurldecode.md) \- Декодування URL-кодованого рядка
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)
