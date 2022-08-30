Змінні HTTP-запиту

-   [FILES](reserved.variables.files.html)
    
-   [SESSION »](reserved.variables.session.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые переменные](reserved.variables.html)
    
-   Змінні HTTP-запиту
    

# REQUEST

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

REQUEST — Змінні запити HTTP

### Опис

Асоціативний масив (array), який за умовчанням містить дані змінних [GET](reserved.variables.get.html) [POST](reserved.variables.post.html) і [COOKIE](reserved.variables.cookies.html)

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

> **Зауваження**
> 
> При роботі в [командному рядку](features.commandline.html) змінні [argv](reserved.variables.argv.html) і [argc](reserved.variables.argc.html) *не* включаються до цього масиву - вони присутні в масиві [SERVER](reserved.variables.server.html)

> **Зауваження**
> 
> Змінні в масиві $REQUEST передаються в скрипт у вигляді методів GET, POST чи COOKIE, тому не можна довіряти, т.к. вони могли бути змінені віддаленим користувачем. Їх наявність та порядок додавання даних у відповідні масиви визначається директивою конфігурації PHP [requestorder](ini.core.html#ini.request-order) і [variablesorder](ini.core.html#ini.variables-order)

### Дивіться також

-   "[Работа с внешними данными](language.variables.external.html)"
-   "[Фільтрування даних](book.filter.html)"