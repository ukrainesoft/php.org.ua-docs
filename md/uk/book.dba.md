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
    -   [dbaclose](function.dba-close.md) — Закриває базу даних DBA
    -   [dbadelete](function.dba-delete.md) — Видаляє запис бази даних, визначену ключем
    -   [dbaexists](function.dba-exists.md) — Перевіряє, чи існує ключ
    -   [dbafetch](function.dba-fetch.md) — Витягує дані за вказаним ключем
    -   [dbafirstkey](function.dba-firstkey.md) — Витягує перший ключ
    -   [dbahandlers](function.dba-handlers.md) - Список всіх доступних обробників
    -   [dbainsert](function.dba-insert.md) - Вставляє запис
    -   [dbakeysplit](function.dba-key-split.md) — Розділяє ключ, заданий у вигляді рядка та створює масив із отриманих частин
    -   [dbalist](function.dba-list.md) - Список всіх відкритих файлів бази даних
    -   [dbanextkey](function.dba-nextkey.md) — Витягує наступний ключ
    -   [dbaopen](function.dba-open.md) — Відкриває базу даних
    -   [dbaoptimize](function.dba-optimize.md) - Оптимізує базу даних
    -   [dbapopen](function.dba-popen.md) — Встановити постійний екземпляр бази даних
    -   [dbareplace](function.dba-replace.md) - Перезаписати або вставити запис
    -   [dbasync](function.dba-sync.md) — Синхронізує базу даних
