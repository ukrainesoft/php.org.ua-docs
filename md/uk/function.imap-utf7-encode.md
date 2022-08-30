Перетворює рядок ISO-8859-1 на модифікований UTF-7

-   [« imaputf7decode](function.imap-utf7-decode.html)
    
-   [imaputf8тоmutf7 »](function.imap-utf8-to-mutf7.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Перетворює рядок ISO-8859-1 на модифікований UTF-7
    

# imaputf7encode

(PHP 4, PHP 5, PHP 7, PHP 8)

imaputf7encode — Перетворює рядок ISO-8859-1 на модифікований UTF-7

### Опис

```methodsynopsis
imap_utf7_encode(string $string): string
```

Перетворює `string` текст у модифікованому кодуванні UTF-7.

Це потрібно для кодування імен поштових скриньок, що містять в імені символи, які не входять до друкованого діапазону ASCII.

### Список параметрів

`string`

Рядок у кодуванні ISO-8859-1.

### Значення, що повертаються

Повертає дані `string` кодовані в модифікованому кодуванні UTF-7, як визначено в [» RFC 2060](http://www.faqs.org/rfcs/rfc2060), Розділ 5.1.3.

### Дивіться також

-   [imaputf7decode()](function.imap-utf7-decode.html) - Декодує рядок із модифікованого кодування UTF-7