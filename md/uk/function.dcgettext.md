Перевизначає одне повідомлення в домені

-   [« bindtextdomain](function.bindtextdomain.md)
    
-   [dcngettext »](function.dcngettext.md)
    
-   [PHP Manual](index.md)
    
-   [Функции gettext](ref.gettext.md)
    
-   Перевизначає одне повідомлення в домені
    

# dcgettext

(PHP 4, PHP 5, PHP 7, PHP 8)

dcgettext — Перевизначення одного повідомлення в домені

### Опис

```methodsynopsis
dcgettext(string $domain, string $message, int $category): string
```

Ця функція дозволяє перевизначити поточний домен для одного повідомлення.

### Список параметрів

`domain`

Домен

`message`

Повідомлення

`category`

Категорія

### Значення, що повертаються

У разі успішного виконання, повертає значення типу string.

### Дивіться також

-   [gettext()](function.gettext.md) - Шукає повідомлення у поточному домені