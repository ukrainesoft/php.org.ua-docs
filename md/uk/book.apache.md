---
navigation:
  - refs.utilspec.server.md: Модулі для роботи з серверами
  - intro.apache.md: Введение »
  - index.md: PHP Manual
  - refs.utilspec.server.md: Модулі для роботи із серверами
title: Apache
---
# Apache

-   [Введение](intro.apache.md)
-   [Встановлення та налаштування](apache.setup.md)
    -   [Вимоги](apache.requirements.md)
    -   [Установка](apache.installation.md)
    -   [Налаштування під час виконання](apache.configuration.md)
    -   [Типи ресурсів](apache.resources.md)
-   [Обумовлені константи](apache.constants.md)
-   [Функции Apache](ref.apache.md)
    -   [apachechildterminate](function.apache-child-terminate.md) — Завершити процес Apache після поточного запиту
    -   [apachegetmodules](function.apache-get-modules.md) — Повертає список завантажених модулів сервера Apache
    -   [apachegetversion](function.apache-get-version.md) — Повертає версію Apache
    -   [apachegetenv](function.apache-getenv.md) — Повертає змінну оточення підпроцесу сервера Apache
    -   [apachelookupuri](function.apache-lookup-uri.md) — Здійснити частковий запит на вказаний URI та повернути усі отримані відомості
    -   [apachenote](function.apache-note.md) — Повертає та встановлює повідомлення до запиту Apache
    -   [apacherequestheaders](function.apache-request-headers.md) — Отримує список усіх заголовків HTTP-запиту
    -   [apacheresponseheaders](function.apache-response-headers.md) — Повертає список усіх заголовків HTTP відповіді Apache
    -   [apachesetenv](function.apache-setenv.md) - Встановлює змінну subprocessenv Apache
    -   [getallheaders](function.getallheaders.md) — Повертає всі заголовки HTTP-запиту
    -   [virtual](function.virtual.md) - Виконує підзапит Apache
