---
navigation:
  - function.rawurldecode.md: « rawurldecode
  - function.urldecode.md: urldecode »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: rawurlencode
---
# rawurlencode

(PHP 4, PHP 5, PHP 7, PHP 8)

rawurlencode — URL-кодування рядка згідно з RFC 3986

### Опис

```methodsynopsis
rawurlencode(string $string): string
```

Кодує рядок згідно [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)

### Список параметрів

`string`

URL, який має бути закодований.

### Значення, що повертаються

Повертає рядок, в якому всі не цифро-літерні символи, крім `-_.~`, повинні бути замінені знаком відсотка (`%`), за яким слідує два шістнадцяткових числа. Це кодування, описане в [» RFC 3986](http://www.faqs.org/rfcs/rfc3986), служить для захисту буквених символів від інтерпретації як спеціальні розмежувачі URL і захищає URL від спотворення при передачі символів з подальшою конвертацією (як у деяких поштових системах).

### Приклади

**Приклад #1 Приклад використання rawurlencode для увімкнення пароля в URL FTP**

```php
<?php
echo '<a href="ftp://user:', rawurlencode('foo @+%/'),
     '@ftp.example.com/x.txt">';
?>
```

Результат виконання цього прикладу:

```
<a href="ftp://user:foo%20%40%2B%25%2F@ftp.example.com/x.txt">
```

Або, якщо ви передаєте інформацію як частину URL:

**Приклад #2 Приклад використання **rawurlencode()****

```php
<?php
echo '<a href="http://example.com/department_list_script/',
    rawurlencode('sales and marketing/Miami'), '">';
?>
```

Результат виконання цього прикладу:

```
<a href="http://example.com/department_list_script/sales%20and%20marketing%2FMiami">
```

### Дивіться також

-   [rawurldecode()](function.rawurldecode.md) - Декодування URL-кодованого рядка
-   [urldecode()](function.urldecode.md) - Декодування URL-кодованого рядка
-   [urlencode()](function.urlencode.md) - URL-кодування рядка
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)
