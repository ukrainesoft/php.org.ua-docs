---
navigation:
  - function.ctype-xdigit.md: « ctype\_xdigit
  - intro.filter.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.vartype.md: 'Модулі, що відносяться до змінних та типів'
title: Фільтрування даних
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Фільтрування даних

-   [Вступ](intro.filter.md)
-   [Встановлення та налаштування](filter.setup.md)
    -   [Вимоги](filter.requirements.md)
    -   [Установка](filter.installation.md)
    -   [Налаштування під час виконання](filter.configuration.md)
    -   [Типи ресурсів](filter.resources.md)
-   [Типи фільтрів](filter.filters.md)
    -   [Фільтри валідації даних](filter.filters.validate.md)
    -   [Очищаючі фільтри](filter.filters.sanitize.md)
    -   [Інші фільтри](filter.filters.misc.md)
    -   [Прапори для фільтрів](filter.filters.flags.md)
-   [Обумовлені константи](filter.constants.md)
-   [Приклади](filter.examples.md)
    -   [Перевірка (валідація)](filter.examples.validation.md)
    -   [Очищення (нормалізація)](filter.examples.sanitization.md)
-   [Функції фільтрації даних](ref.filter.md)
    -   [filter\_has\_var](function.filter-has-var.md) \- Перевіряє існування змінної зазначеного типу
    -   [filter\_id](function.filter-id.md)— Повертає ідентифікатор, який належить іменованому фільтру
    -   [filter\_input\_array](function.filter-input-array.md)— Отримує кілька змінних ззовні PHP і, за необхідності, фільтрує їх
    -   [filter\_input](function.filter-input.md) \- Приймає змінну ззовні PHP і, при необхідності, фільтрує її
    -   [filter\_list](function.filter-list.md)— Повертає список усіх підтримуваних фільтрів
    -   [filter\_var\_array](function.filter-var-array.md)— Приймає кілька змінних і, за потреби, фільтрує їх
    -   [filter\_var](function.filter-var.md)— Фільтрує змінну за допомогою певного фільтра
