Декодує рядок із модифікованого кодування UTF-7

-   [« imap\_unsubscribe](function.imap-unsubscribe.html)
    
-   [imap\_utf7\_encode »](function.imap-utf7-encode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Декодує рядок із модифікованого кодування UTF-7
    

# imaputf7decode

(PHP 4, PHP 5, PHP 7, PHP 8)

imaputf7decode — Декодує рядок із модифікованого кодування UTF-7

### Опис

```methodsynopsis
imap_utf7_decode(string $string): string|false
```

Декодує `string` з модифікованого кодування UTF-7 ISO-8859-1.

Це потрібно для декодування імен поштових скриньок, що містять у імені символи, які не входять до друкованого діапазону ASCII.

### Список параметрів

`string`

Текст у модифікованому кодуванні UTF-7, як визначено в [» RFC 2060](http://www.faqs.org/rfcs/rfc2060), Розділ 5.1.3.

### Значення, що повертаються

Повертає рядок у кодуванні ISO-8859-1, який містить ту ж послідовність символів, що й `string`, або **`false`**, якщо `string` містить некоректні символи або якщо `string` містить символи, що не входять до набору символів ISO-8859-1.

### Дивіться також

-   [imap\_utf7\_encode()](function.imap-utf7-encode.html) - Перетворює рядок ISO-8859-1 на модифікований UTF-7