---
navigation:
  - refs.database.abstract.md: « Рівні абстракції
  - intro.dba.md: Введение »
  - index.md: PHP Manual
  - refs.database.abstract.md: Рівні абстракції
title: Database (dbm-style) Abstraction Layer
---
# Database (dbm-style) Abstraction Layer

-   [Введение](intro.dba.md)
-   [Встановлення та налаштування](dba.setup.md)
    -   [Вимоги](dba.requirements.md)
    -   [Установка](dba.installation.md)
    -   [Налаштування під час виконання](dba.configuration.md)
    -   [Типи ресурсів](dba.resources.md)
-   [Обумовлені константи](dba.constants.md)
-   [Приклади](dba.examples.md)
    -   [Базовое использование](dba.example.md)
-   [Функції DBA](ref.dba.md)
    -   [dbaclose](function.dba-close.html) — Закриває базу даних DBA
    -   [dbadelete](function.dba-delete.html) — Видаляє запис бази даних, визначену ключем
    -   [dbaexists](function.dba-exists.html) — Перевіряє, чи існує ключ
    -   [dbafetch](function.dba-fetch.html) — Витягує дані за вказаним ключем
    -   [dbafirstkey](function.dba-firstkey.html) — Витягує перший ключ
    -   [dbahandlers](function.dba-handlers.html) - Список всіх доступних обробників
    -   [dbainsert](function.dba-insert.html) - Вставляє запис
    -   [dbakeysplit](function.dba-key-split.html) — Розділяє ключ, заданий у вигляді рядка та створює масив із отриманих частин
    -   [dbalist](function.dba-list.html) - Список всіх відкритих файлів бази даних
    -   [dbanextkey](function.dba-nextkey.html) — Витягує наступний ключ
    -   [dbaopen](function.dba-open.html) — Відкриває базу даних
    -   [dbaoptimize](function.dba-optimize.html) - Оптимізує базу даних
    -   [dbapopen](function.dba-popen.html) — Встановити постійний екземпляр бази даних
    -   [dbareplace](function.dba-replace.html) - Перезаписати або вставити запис
    -   [dbasync](function.dba-sync.html) — Синхронізує базу даних
