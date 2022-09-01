---
navigation:
  - reserved.variables.md: «Зумовлені змінні
  - reserved.variables.globals.md: $GLOBALS »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: Суперглобальні змінні
---
# Суперглобальні змінні

Суперглобальні змінні — Вбудовані змінні, які завжди доступні в усіх сферах.

### Опис

Деякі визначені змінні PHP є "суперглобальними", що означає, що вони доступні в будь-якому місці скрипта. Немає необхідності використовувати синтаксис **global $variable;** для доступу до них у функціях та методах.

Суперглобальними змінними є:

-   [$GLOBALS](reserved.variables.globals.md)
-   [SERVER](reserved.variables.server.md)
-   [GET](reserved.variables.get.md)
-   [POST](reserved.variables.post.md)
-   [FILES](reserved.variables.files.md)
-   [COOKIE](reserved.variables.cookies.md)
-   [SESSION](reserved.variables.session.md)
-   [REQUEST](reserved.variables.request.md)
-   [ENV](reserved.variables.environment.md)

### Примітки

> **Зауваження** **Доступність змінних**
> 
> За замовчуванням усі суперглобальні змінні доступні завжди, проте існують налаштування, які можуть впливати на це. За подальшою інформацією звертайтесь до опису директиви [variablesorder](ini.core.html#ini.variables-order)

> **Зауваження** **Змінні змінних**
> 
> Суперглобальні змінні не можуть бути використані як [змінних змінних](language.variables.variable.md) всередині функцій та методів.

### Дивіться також

-   [Область видимості змінної](language.variables.scope.md)
-   Директива [variablesorder](ini.core.html#ini.variables-order)
-   "[Фільтрування даних](book.filter.md)"
