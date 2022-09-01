---
navigation:
  - function.rawurlencode.html: « rawurlencode
  - function.urlencode.html: urlencode »
  - index.html: PHP Manual
  - ref.url.html: Функції URL
title: urldecode
---
# urldecode

(PHP 4, PHP 5, PHP 7, PHP 8)

urldecode — Декодування URL-кодованого рядка

### Опис

```methodsynopsis
urldecode(string $string): string
```

Декодує будь-які кодовані послідовності `%##` у цьому рядку. Символ "плюс" ('`+`') декодується в символ пробілу.

### Список параметрів

`string`

Рядок, який має бути декодований.

### Значення, що повертаються

Повертає декодований рядок.

### Приклади

**Приклад #1 Приклад використання **urldecode()****

```php
<?php
$query = "my=apples&are=green+and+red";

foreach (explode('&', $query) as $chunk) {
    $param = explode("=", $chunk);

    if ($param) {
        printf("Значение параметра \"%s\" - \"%s\"<br/>\n", urldecode($param[0]), urldecode($param[1]));
    }
}
?>
```

### Примітки

**Увага**

Змінні у суперглобальних масивах [GET](reserved.variables.get.html) і [REQUEST](reserved.variables.request.html) вже декодовані. Застосування **urldecode()** до елементів [GET](reserved.variables.get.html) або [REQUEST](reserved.variables.request.md) може призвести до несподіваних та небезпечних результатів.

### Дивіться також

-   [urlencode()](function.urlencode.md) - URL-кодування рядка
-   [rawurlencode()](function.rawurlencode.md) - URL-кодування рядка згідно з RFC 3986
-   [rawurldecode()](function.rawurldecode.md) - Декодування URL-кодованого рядка
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)
