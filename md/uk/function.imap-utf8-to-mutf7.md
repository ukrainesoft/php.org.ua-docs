Кодувати рядок UTF-8 у змінений UTF-7

-   [« imaputf7encode](function.imap-utf7-encode.html)
    
-   [imaputf8 »](function.imap-utf8.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Кодувати рядок UTF-8 у змінений UTF-7
    

# imaputf8тоmutf7

(PHP 5> = 5.3.0, PHP 7, PHP 8)

imaputf8тоmutf7 — Кодувати рядок UTF-8 у змінений UTF-7

### Опис

```methodsynopsis
imap_utf8_to_mutf7(string $string): string|false
```

Кодувати рядок UTF-8 у змінений рядок UTF-7 (відповідно до RFC 2060, розділ 5.1.3).

> **Зауваження**
> 
> Ця функція доступна лише у випадку, якщо libcclient експортує utf8тоmutf7().

### Список параметрів

`string`

Закодований у UTF-8 рядок.

### Значення, що повертаються

Повертає `string`, конвертовану в змінену UTF-7 або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imapmutf7тоutf8()](function.imap-mutf7-to-utf8.html) - Декодувати змінений рядок UTF-7 у UTF-8