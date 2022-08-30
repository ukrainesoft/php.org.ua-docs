URL-кодування рядка

-   [« urldecode](function.urldecode.md)
    
-   [V8js »](book.v8js.md)
    
-   [PHP Manual](index.md)
    
-   [Функції URL](ref.url.md)
    
-   URL-кодування рядка
    

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

Повертає рядок, в якому всі не цифро-літерні символи, крім `-_.` повинні бути замінені знаком відсотка (`%`), за яким слідує два шістнадцяткових числа, а пробіли закодовані як знак додавання (`+`). Рядок кодується тим же способом, що й POST-дані веб-форми, тобто за типом контенту `application/x-www-form-urlencoded`. Це відрізняється від кодування по [» RFC 3986](http://www.faqs.org/rfcs/rfc3986) (дивіться [rawurlencode()](function.rawurlencode.md) ) в тому, що з історичних причин пробіли кодуються як знак "плюс" (+).

### Приклади

**Приклад #1 Приклад використання **urlencode()****

```php
<?php
echo '<a href="mycgi?foo=', urlencode($userinput), '">';
?>
```

**Приклад #2 Приклад використання **urlencode()** і [htmlentities()](function.htmlentities.md)**

```php
<?php
$query_string = 'foo=' . urlencode($foo) . '&bar=' . urlencode($bar);
echo '<a href="mycgi?' . htmlentities($query_string) . '">';
?>
```

### Примітки

> **Зауваження**
> 
> Будьте уважні зі змінними, які можуть збігатися з елементами HTML. Такі сутності як &, © та £ розбираються браузером і використовується як реальна сутність, а не бажане ім'я змінної. Це очевидний конфлікт, який W3C вказує протягом багатьох років. Дивіться подробиці: [» http://www.w3.org/TR/html4/appendix/notes.html#h-B.2.2](http://www.w3.org/TR/html4/appendix/notes.html#h-B.2.2)
> 
> PHP підтримує зміну роздільника аргументів на рекомендований W3C символ "точку з комою" шляхом зміни директиви argseparator у файлі .ini. На жаль, більшість додатків користувача не відправляють дані форми у форматі з роздільником "точка з комою". Більше переносимий спосіб вирішити цю проблему - це використовувати & замість & як роздільник. Вам не потрібно буде для цього змінювати PHP-директиву argseparator. Залишіть розділювач як &, але кодуйте ваші URL-адреси за допомогою [htmlentities()](function.htmlentities.md) або [htmlspecialchars()](function.htmlspecialchars.md)

### Дивіться також

-   [urldecode()](function.urldecode.md) - Декодування URL-кодованого рядка
-   [htmlentities()](function.htmlentities.md) - Перетворює всі можливі символи у відповідні HTML-сутності
-   [rawurlencode()](function.rawurlencode.md) - URL-кодування рядка згідно з RFC 3986
-   [rawurldecode()](function.rawurldecode.md) - Декодування URL-кодованого рядка
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)