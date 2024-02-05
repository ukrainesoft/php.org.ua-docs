---
navigation:
  - function.rawurlencode.md: « rawurlencode
  - function.urlencode.md: urlencode »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: urldecode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# urldecode

(PHP 4, PHP 5, PHP 7, PHP 8)

urldecode — Декодування URL-кодованого рядка

### Опис

```methodsynopsis
urldecode(string $string): string
```

Декодує будь-які кодовані послідовності `%##` у цьому рядку. Символ "плюс" ('`+` ') декодується в символ пробілу.

### Список параметрів

`string`

Рядок, який має бути декодований.

### Значення, що повертаються

Повертає декодований рядок.

### Приклади

**Приклад #1 Приклад використання** urldecode()\*\*\*\*

```php
<?php
$query = "my=apples&are=green+and+red";

foreach (explode('&', $query) as $chunk) {
    $param = explode("=", $chunk);

    if ($param) {
        printf("Значение параметра \"%s\" - \"%s\"<br/>\n", urldecode($param[0]), urldecode($param[1]));
    }
}
?>
```

### Примітки

**Увага**

Змінні у суперглобальних масивах [$\_GET](reserved.variables.get.md) і [$\_REQUEST](reserved.variables.request.md) вже декодовані. Застосування **urldecode()** до елементів [$\_GET](reserved.variables.get.md) або [$\_REQUEST](reserved.variables.request.md) може призвести до несподіваних та небезпечних результатів.

### Дивіться також

-   [urlencode()](function.urlencode.md) \- URL-кодування рядка
-   [rawurlencode()](function.rawurlencode.md) \- URL-кодування рядка згідно з RFC 3986
-   [rawurldecode()](function.rawurldecode.md) \- Декодування URL-кодованого рядка
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)
