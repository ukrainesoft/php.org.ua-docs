---
navigation:
  - migration70.constants.md: « Нові глобальні константи
  - migration70.removed-exts-sapis.md: Віддалені модулі та SAPI »
  - index.md: PHP Manual
  - migration70.md: Міграція з PHP 5.6.x на PHP 7.0.x
title: Зміни у модулях SAPI
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Зміни у модулях SAPI

### [FPM](book.fpm.md)

#### Не повністю визначений порт [listen](install.fpm.configuration.md#listen) тепер слухає як IPv4, так і IPv6

У PHP 5 директива [listen](install.fpm.configuration.md#listen) що містить тільки номер порту, призводила до прослуховування всіх інтерфейсів, але тільки IPv4. PHP 7 тепер прийматиме як з IPv4, так і з IPv6.

Це не впливає на директиви, що містять конкретні IP-адреси.
