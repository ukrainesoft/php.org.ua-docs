Зміни у модулях SAPI

-   [« Нові глобальні константи](migration70.constants.md)
    
-   [Віддалені модулі та SAPI »](migration70.removed-exts-sapis.html)
    
-   [PHP Manual](index.md)
    
-   [Миграция с PHP 5.6.x на PHP 7.0.x](migration70.md)
    
-   Зміни у модулях SAPI
    

## Зміни у модулях SAPI

### [FPM](book.fpm.md)

#### Не повністю визначений порт [listen](install.fpm.configuration.html#listen) тепер слухає як IPv4, так і IPv6

У PHP 5 директива [listen](install.fpm.configuration.html#listen) що містить тільки номер порту, призводила до прослуховування всіх інтерфейсів, але тільки IPv4. PHP 7 тепер прийматиме як з IPv4, так і з IPv6.

Це не впливає на директиви, які містять конкретні IP-адреси.