---
navigation:
  - pgsql.requirements.md: « Вимоги
  - pgsql.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - pgsql.setup.md: Встановлення та налаштування
title: Встановлення
---
## Встановлення

Для того, щоб увімкнути підтримку PostgreSQL, необхідно скомпілювати PHP з директивою **\-with-pgsql=DIR**. Параметр `DIR` визначає шлях до настановної директорії PostgreSQL, за умовчанням це /usr/local/pgsql. Якщо доступний динамічний модуль, він може бути включений директивою [extension](ini.core.md#ini.extension) у php.ini, або функцією [dl()](function.dl.md)
