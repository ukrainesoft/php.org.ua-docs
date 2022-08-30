Декодування URL-кодованого рядка

-   [« parseurl](function.parse-url.html)
    
-   [rawurlencode »](function.rawurlencode.html)
    
-   [PHP Manual](index.html)
    
-   [Функції URL](ref.url.html)
    
-   Декодування URL-кодованого рядка
    

# rawurldecode

(PHP 4, PHP 5, PHP 7, PHP 8)

rawurldecode — Декодування URL-кодованого рядка

### Опис

```methodsynopsis
rawurldecode(string $string): string
```

Повертає рядок, у якому послідовність знаків відсотка (`%`) та наступні за ним два шістнадцяткові числа замінені буквальними символами.

### Список параметрів

`string`

URL, який має бути декодований.

### Значення, що повертаються

Повертає декодовану URL-адресу у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **rawurldecode()****

```php
<?php

echo rawurldecode('foo%20bar%40baz'); // foo bar@baz

?>
```

### Примітки

> **Зауваження**
> 
> **rawurldecode()** не декодує символ додавання ('+') у пробіли. Це робить [urldecode()](function.urldecode.html)

### Дивіться також

-   [rawurlencode()](function.rawurlencode.html) - URL-кодування рядка згідно з RFC 3986
-   [urldecode()](function.urldecode.html) - Декодування URL-кодованого рядка
-   [urlencode()](function.urlencode.html) - URL-кодування рядка
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)