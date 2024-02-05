---
navigation:
  - pgsql.requirements.md: « Вимоги
  - pgsql.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - pgsql.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Для того, щоб увімкнути підтримку PostgreSQL, необхідно скомпілювати PHP з директивою \*\*--with-pgsql\[=DIR\]\*\*Параметр`DIR` визначає шлях до настановної директорії PostgreSQL, за умовчанням це /usr/local/pgsql. Якщо доступний динамічний модуль, він може бути включений директивою [extension](ini.core.md#ini.extension)в php.ini, либо функцией[dl()](function.dl.md)
