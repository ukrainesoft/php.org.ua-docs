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
-   [$\_SERVER](reserved.variables.server.html)
-   [$\_GET](reserved.variables.get.html)
-   [$\_POST](reserved.variables.post.html)
-   [$\_FILES](reserved.variables.files.html)
-   [$\_COOKIE](reserved.variables.cookies.html)
-   [$\_SESSION](reserved.variables.session.html)
-   [$\_REQUEST](reserved.variables.request.html)
-   [$\_ENV](reserved.variables.environment.html)

### Примітки

> **Зауваження** **Доступність змінних**
> 
> За замовчуванням усі суперглобальні змінні доступні завжди, проте існують налаштування, які можуть впливати на це. За подальшою інформацією звертайтесь до опису директиви [variables\_order](ini.core.html#ini.variables-order)

> **Зауваження** **Змінні змінних**
> 
> Суперглобальні змінні не можуть бути використані як [переменных переменных](language.variables.variable.html) всередині функцій та методів.

### Дивіться також

-   [Область видимости переменной](language.variables.scope.html)
-   Директива [variables\_order](ini.core.html#ini.variables-order)
-   "[Фильтрация данных](book.filter.html)"