---
navigation:
  - refs.database.abstract.md: « Рівні абстракції
  - intro.dba.md: Вступ "
  - index.md: PHP Manual
  - refs.database.abstract.md: Рівні абстракції
title: Database (dbm-style) Abstraction Layer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Database (dbm-style) Abstraction Layer

-   [Вступ](intro.dba.md)
-   [Встановлення та налаштування](dba.setup.md)
    -   [Вимоги](dba.requirements.md)
    -   [Установка](dba.installation.md)
    -   [Налаштування під час виконання](dba.configuration.md)
    -   [Типи ресурсів](dba.resources.md)
-   [Обумовлені константи](dba.constants.md)
-   [Приклади](dba.examples.md)
    -   [Базове використання](dba.example.md)
-   [Функції DBA](ref.dba.md)
    -   [dba\_close](function.dba-close.md)— Закриває базу даних DBA
    -   [dba\_delete](function.dba-delete.md)— Видаляє запис бази даних, визначену ключем
    -   [dba\_exists](function.dba-exists.md)— Перевіряє, чи існує ключ
    -   [dba\_fetch](function.dba-fetch.md)— Витягує дані за вказаним ключем
    -   [dba\_firstkey](function.dba-firstkey.md)— Витягує перший ключ
    -   [dba\_handlers](function.dba-handlers.md) \- Список всіх доступних обробників
    -   [dba\_insert](function.dba-insert.md) \- Вставляє запис
    -   [dba\_key\_split](function.dba-key-split.md)— Розділяє ключ, заданий у вигляді рядка та створює масив із отриманих частин
    -   [dba\_list](function.dba-list.md) \- Список всіх відкритих файлів бази даних
    -   [dba\_nextkey](function.dba-nextkey.md)— Витягує наступний ключ
    -   [dba\_open](function.dba-open.md)— Відкриває базу даних
    -   [dba\_optimize](function.dba-optimize.md) \- Оптимізує базу даних
    -   [dba\_popen](function.dba-popen.md)— Встановити постійний екземпляр бази даних
    -   [dba\_replace](function.dba-replace.md) \- Перезаписати або вставити запис
    -   [dba\_sync](function.dba-sync.md)— Синхронізує базу даних
