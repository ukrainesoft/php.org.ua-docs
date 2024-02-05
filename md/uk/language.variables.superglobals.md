---
navigation:
  - reserved.variables.md: «Зумовлені змінні
  - reserved.variables.globals.md: $GLOBALS »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: Суперглобальні змінні
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Суперглобальні змінні

Суперглобальні змінні — Вбудовані змінні, які завжди доступні у всіх областях

### Опис

Деякі визначені змінні PHP є "суперглобальними", що означає, що вони доступні в будь-якому місці скрипта. Немає необхідності використовувати синтаксис **global $variable;** для доступу до них у функціях та методах.

Суперглобальними змінними є:

-   [$GLOBALS](reserved.variables.globals.md)
-   [$\_SERVER](reserved.variables.server.md)
-   [$\_GET](reserved.variables.get.md)
-   [$\_POST](reserved.variables.post.md)
-   [$\_FILES](reserved.variables.files.md)
-   [$\_COOKIE](reserved.variables.cookies.md)
-   [$\_SESSION](reserved.variables.session.md)
-   [$\_REQUEST](reserved.variables.request.md)
-   [$\_ENV](reserved.variables.environment.md)

### Примітки

> **Зауваження** **Доступність змінних**
> 
> За замовчуванням усі суперглобальні змінні доступні завжди, проте існують налаштування, які можуть впливати на це. За подальшою інформацією звертайтесь до опису директиви [variables\_order](ini.core.md#ini.variables-order)

> **Зауваження** **Змінні змінних**
> 
> Суперглобальні змінні не можуть бути використані як [змінних змінних](language.variables.variable.md) всередині функцій та методів.

### Дивіться також

-   [Область видимості змінної](language.variables.scope.md)
-   Директива[variables\_order](ini.core.md#ini.variables-order)
-   "[Фільтрування даних](book.filter.md)"
