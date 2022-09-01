---
navigation:
  - pgsql.requirements.html: « Вимоги
  - pgsql.configuration.html: Налаштування під час виконання »
  - index.html: PHP Manual
  - pgsql.setup.html: Встановлення та налаштування
title: Встановлення
---
## Встановлення

Для того, щоб увімкнути підтримку PostgreSQL, необхідно скомпілювати PHP з директивою **\-with-pgsql=DIR**. Параметр `DIR` визначає шлях до настановної директорії PostgreSQL, за умовчанням це /usr/local/pgsql. Якщо доступний динамічний модуль, він може бути включений директивою [extension](ini.core.html#ini.extension) у php.ini, або функцією [dl()](function.dl.html)
