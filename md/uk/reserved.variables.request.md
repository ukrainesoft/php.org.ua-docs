Змінні HTTP-запиту

-   [« $\_FILES](reserved.variables.files.html)
    
-   [$\_SESSION »](reserved.variables.session.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые переменные](reserved.variables.html)
    
-   Змінні HTTP-запиту
    

# REQUEST

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

REQUEST — Змінні запити HTTP

### Опис

Асоціативний масив (array), який за умовчанням містить дані змінних [$\_GET](reserved.variables.get.html) [$\_POST](reserved.variables.post.html) і [$\_COOKIE](reserved.variables.cookies.html)

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

> **Зауваження**
> 
> При роботі в [командной строке](features.commandline.html) змінні [argv](reserved.variables.argv.html) і [argc](reserved.variables.argc.html) *не* включаються до цього масиву - вони присутні в масиві [$\_SERVER](reserved.variables.server.html)

> **Зауваження**
> 
> Змінні в масиві $REQUEST передаються в скрипт у вигляді методів GET, POST чи COOKIE, тому не можна довіряти, т.к. вони могли бути змінені віддаленим користувачем. Їх наявність та порядок додавання даних у відповідні масиви визначається директивою конфігурації PHP [request\_order](ini.core.html#ini.request-order) і [variables\_order](ini.core.html#ini.variables-order)

### Дивіться також

-   "[Работа с внешними данными](language.variables.external.html)"
-   "[Фильтрация данных](book.filter.html)"