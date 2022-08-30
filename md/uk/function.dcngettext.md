Версія dcgettext для множини

-   [« dcgettext](function.dcgettext.md)
    
-   [dgettext »](function.dgettext.md)
    
-   [PHP Manual](index.md)
    
-   [Функции gettext](ref.gettext.md)
    
-   Версія dcgettext для множини
    

# dcngettext

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

dcngettext — Версія dcgettext для множини

### Опис

```methodsynopsis
dcngettext(    string $domain,    string $singular,    string $plural,    int $count,    int $category): string
```

Ця функція дозволяє перевизначити одне повідомлення з використанням множини в поточному домені.

### Список параметрів

`domain`

Домен.

`singular`

`plural`

`count`

`category`

### Значення, що повертаються

У разі успішного виконання повертає рядок (string).

### Дивіться також

-   [ngettext()](function.ngettext.md) - Версія gettext для повідомлень у множині