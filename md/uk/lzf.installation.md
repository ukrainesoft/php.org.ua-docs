---
navigation:
  - lzf.requirements.md: « Вимоги
  - lzf.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - lzf.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Цей модуль [» PECL](https://pecl.php.net/) не постачається разом з PHP. Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Встановлення PECL модулів](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/lzf](https://pecl.php.net/package/lzf)

Для використання цього модуля необхідно скомпілювати PHP з підтримкою lzf, використовуючи ключ конфігурації **\--with-lzf\[=DIR\]**. Також ви можете вказати ключ **\--enable-lzf-better-compression** для оптимізації LZF для кращого стиснення на шкоду швидкості роботи.

Користувачі Windows повинні дозволити php\_lzf.dll у php.ini. DLL для цього модуля PECL поки що недоступна. Дивіться також розділ [збирання на Windows](install.windows.building.md)
