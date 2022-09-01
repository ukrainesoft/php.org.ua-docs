---
navigation:
  - function.ctype-xdigit.html: « ctypexdigit
  - intro.filter.md: Введение »
  - index.md: PHP Manual
  - refs.basic.vartype.md: 'Модулі, що відносяться до змінних та типів'
title: Фільтрування даних
---
# Фільтрування даних

-   [Введение](intro.filter.md)
-   [Встановлення та налаштування](filter.setup.md)
    -   [Вимоги](filter.requirements.md)
    -   [Установка](filter.installation.md)
    -   [Налаштування під час виконання](filter.configuration.md)
    -   [Типи ресурсів](filter.resources.md)
-   [Типи фільтрів](filter.filters.md)
    -   [Фільтри валідації даних](filter.filters.validate.md)
    -   [Очищаючі фільтри](filter.filters.sanitize.md)
    -   [Інші фільтри](filter.filters.misc.md)
    -   [Прапори, що використовуються у фільтрах](filter.filters.flags.md)
-   [Обумовлені константи](filter.constants.md)
-   [Приклади](filter.examples.md)
    -   [Перевірка (валідація)](filter.examples.validation.md)
    -   [Очищення (нормалізація)](filter.examples.sanitization.md)
-   [Функції фільтрації даних](ref.filter.md)
    -   [filterhasvar](function.filter-has-var.md) - Перевіряє існування змінної зазначеного типу
    -   [filterід](function.filter-id.md) — Повертає ідентифікатор, який належить іменованому фільтру
    -   [filterinputarray](function.filter-input-array.md) — Отримує кілька змінних ззовні PHP і, за потреби, фільтрує їх
    -   [filterinput](function.filter-input.md) - Приймає змінну ззовні PHP і, при необхідності, фільтрує її
    -   [filterlist](function.filter-list.md) — Повертає список усіх підтримуваних фільтрів
    -   [filtervararray](function.filter-var-array.md) — Приймає кілька змінних і, за потреби, фільтрує їх
    -   [filtervar](function.filter-var.md) — Фільтрує змінну за допомогою певного фільтра
