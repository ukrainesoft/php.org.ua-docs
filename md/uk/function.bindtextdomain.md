Встановлює або отримує шлях для домену

-   [« bindtextdomaincodeset](function.bind-textdomain-codeset.html)
    
-   [dcgettext »](function.dcgettext.html)
    
-   [PHP Manual](index.html)
    
-   [Функции gettext](ref.gettext.html)
    
-   Встановлює або отримує шлях для домену
    

# bindtextdomain

(PHP 4, PHP 5, PHP 7, PHP 8)

bindtextdomain — Встановлює або отримує шлях для домену

### Опис

```methodsynopsis
bindtextdomain(string $domain, ?string $directory): string|false
```

Функція **bindtextdomain()** встановлює чи отримує шлях для домену.

### Список параметрів

`domain`

Домен.

`directory`

Шлях до директорії. Порожній рядок означає поточний каталог. Якщо **`null`**, повертається поточний встановлений каталог.

### Значення, що повертаються

Повний шлях для домену, встановленого параметром `domain` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------|
|        | `directory` тепер допускає значення null. Раніше неможливо було отримати поточний встановлений каталог. |

### Приклади

**Приклад #1 Приклад використання **bindtextdomain()****

```php
<?php

$domain = 'myapp';
echo bindtextdomain($domain, '/usr/share/myapp/locale');

?>
```

Результат виконання цього прикладу:

```
/usr/share/myapp/locale
```

### Примітки

> **Зауваження**
> 
> Інформація **bindtextdomain()** зберігається кожному за процесу, а чи не для потоку.