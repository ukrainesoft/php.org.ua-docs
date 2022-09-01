---
navigation:
  - reserved.variables.files.md: FILES
  - reserved.variables.session.md: SESSION »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: REQUEST
---
# REQUEST

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

REQUEST — Змінні запити HTTP

### Опис

Асоціативний масив (array), який за умовчанням містить дані змінних [GET](reserved.variables.get.md) [POST](reserved.variables.post.md) і [COOKIE](reserved.variables.cookies.md)

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

> **Зауваження**
> 
> При роботі в [командному рядку](features.commandline.md) змінні [argv](reserved.variables.argv.md) і [argc](reserved.variables.argc.md) *не* включаються до цього масиву - вони присутні в масиві [SERVER](reserved.variables.server.md)

> **Зауваження**
> 
> Змінні в масиві $REQUEST передаються в скрипт у вигляді методів GET, POST чи COOKIE, тому не можна довіряти, т.к. вони могли бути змінені віддаленим користувачем. Їх наявність та порядок додавання даних у відповідні масиви визначається директивою конфігурації PHP [requestorder](ini.core.html#ini.request-order) і [variablesorder](ini.core.html#ini.variables-order)

### Дивіться також

-   "[Робота із зовнішніми даними](language.variables.external.md)"
-   "[Фільтрування даних](book.filter.md)"
