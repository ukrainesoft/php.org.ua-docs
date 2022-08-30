Зміни у модулях SAPI

-   [« Новые глобальные константы](migration70.constants.html)
    
-   [Віддалені модулі та SAPI »](migration70.removed-exts-sapis.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 5.6.x на PHP 7.0.x](migration70.html)
    
-   Зміни у модулях SAPI
    

## Зміни у модулях SAPI

### [FPM](book.fpm.html)

#### Не повністю визначений порт [listen](install.fpm.configuration.html#listen) тепер слухає як IPv4, так і IPv6

У PHP 5 директива [listen](install.fpm.configuration.html#listen) що містить тільки номер порту, призводила до прослуховування всіх інтерфейсів, але тільки IPv4. PHP 7 тепер прийматиме як з IPv4, так і з IPv6.

Це не впливає на директиви, які містять конкретні IP-адреси.