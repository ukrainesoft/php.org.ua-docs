---
navigation:
  - reserved.variables.files.md: « $\_FILES
  - reserved.variables.session.md: $\_SESSION »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $\_REQUEST
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $\_REQUEST

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_REQUEST — Змінні запити HTTP

### Опис

Асоціативний масив (array), який за умовчанням містить дані змінних [$\_GET](reserved.variables.get.md) [$\_POST](reserved.variables.post.md) і [$\_COOKIE](reserved.variables.cookies.md)

### Примітки

> **Зауваження** :
> 
> Це «суперглобальна» чи автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

> **Зауваження** :
> 
> При работе в[командному рядку](features.commandline.md) змінні [argv](reserved.variables.argv.md) і [argc](reserved.variables.argc.md) *не* включаються до цього масиву - вони присутні в масиві [$\_SERVER](reserved.variables.server.md)

> **Зауваження** :
> 
> Змінні в масиві $\_REQUEST передаються у скрипт у вигляді методів GET, POST чи COOKIE, тому не можна довіряти, т.к. вони могли бути змінені віддаленим користувачем. Їх наявність та порядок додавання даних у відповідні масиви визначається директивою конфігурації PHP [request\_order](ini.core.md#ini.request-order) і [variables\_order](ini.core.md#ini.variables-order)

### Дивіться також

-   "[Робота із зовнішніми даними](language.variables.external.md)"
-   "[Фільтрування даних](book.filter.md)"
