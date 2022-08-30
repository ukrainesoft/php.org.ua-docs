Вбудовані змінні, які завжди доступні у всіх областях

-   [« Предопределённые переменные](reserved.variables.html)
    
-   [$GLOBALS »](reserved.variables.globals.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые переменные](reserved.variables.html)
    
-   Вбудовані змінні, які завжди доступні у всіх областях
    

# Суперглобальні змінні

Суперглобальні змінні — Вбудовані змінні, які завжди доступні в усіх сферах.

### Опис

Деякі визначені змінні PHP є "суперглобальними", що означає, що вони доступні в будь-якому місці скрипта. Немає необхідності використовувати синтаксис **global $variable;** для доступу до них у функціях та методах.

Суперглобальними змінними є:

-   [$GLOBALS](reserved.variables.globals.html)
-   [SERVER](reserved.variables.server.html)
-   [GET](reserved.variables.get.html)
-   [POST](reserved.variables.post.html)
-   [FILES](reserved.variables.files.html)
-   [COOKIE](reserved.variables.cookies.html)
-   [SESSION](reserved.variables.session.html)
-   [REQUEST](reserved.variables.request.html)
-   [ENV](reserved.variables.environment.html)

### Примітки

> **Зауваження** **Доступність змінних**
> 
> За замовчуванням усі суперглобальні змінні доступні завжди, проте існують налаштування, які можуть впливати на це. За подальшою інформацією звертайтесь до опису директиви [variablesorder](ini.core.html#ini.variables-order)

> **Зауваження** **Змінні змінних**
> 
> Суперглобальні змінні не можуть бути використані як [переменных переменных](language.variables.variable.html) всередині функцій та методів.

### Дивіться також

-   [Область видимості змінної](language.variables.scope.html)
-   Директива [variablesorder](ini.core.html#ini.variables-order)
-   "[Фільтрування даних](book.filter.html)"