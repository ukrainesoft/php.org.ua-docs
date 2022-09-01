---
navigation:
  - lzf.requirements.html: « Вимоги
  - lzf.configuration.html: Налаштування під час виконання »
  - index.html: PHP Manual
  - lzf.setup.html: Встановлення та налаштування
title: Встановлення
---
## Встановлення

Цей модуль [» PECL](https://pecl.php.net/) не постачається разом з PHP. Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Установка PECL модулей](install.pecl.html). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/lzf](https://pecl.php.net/package/lzf)

Для використання цього модуля необхідно скомпілювати PHP з підтримкою lzf, використовуючи ключ конфігурації **\-with-lzf=DIR**. Також ви можете вказати ключ **\-enable-lzf-better-compression** для оптимізації LZF для кращого стиснення на шкоду швидкості роботи.

Користувачі Windows повинні дозволити phplzf.dll у php.ini. DLL для цього модуля PECL зараз недоступна. Дивіться також розділ [сборка на Windows](install.windows.building.html)
