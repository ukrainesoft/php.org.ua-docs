---
navigation:
  - password.requirements.md: « Вимоги
  - password.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - password.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Для використання цих функцій не потрібне проведення установки, оскільки вони є частиною ядра PHP.

Однак, щоб увімкнути хешування використовуючи Argon2, PHP має зібраний за допомогою libargon2 з використанням опції конфігурації **\--with-password-argon2**

До PHP 8.1.0 можна було вказати каталог argon2 за допомогою команди **\--with-password-argon2\[=DIR\]**
