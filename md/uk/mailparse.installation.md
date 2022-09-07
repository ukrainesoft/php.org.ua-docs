---
navigation:
  - mailparse.requirements.md: « Вимоги
  - mailparse.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - mailparse.setup.md: Встановлення та налаштування
title: Встановлення
---
## Встановлення

Цей модуль [» PECL](https://pecl.php.net/) не постачається разом з PHP. Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Установка PECL модулей](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/mailparse](https://pecl.php.net/package/mailparse)

Для використання цих функцій ви повинні скомпілювати PHP з підтримкою mailparse, використовуючи опцію конфігурації **\-enable-mailparse**

Користувачам Windows необхідно дозволити phpmailparse.dll у php.ini для використання цих функцій. Бінарні файли Windows (DLL-файли) для цього модуля PECL доступні на сайті PECL.

Необхідно, щоб модуль [mbstring](ref.mbstring.md) був завантажений перед використанням `mailparse`
