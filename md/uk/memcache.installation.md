---
navigation:
  - memcache.requirements.md: « Вимоги
  - memcache.ini.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - memcache.setup.md: Встановлення та налаштування
title: Встановлення
---
## Встановлення

Цей модуль [» PECL](https://pecl.php.net/) не постачається разом з PHP. Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Установка PECL модулей](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/memcache](https://pecl.php.net/package/memcache)

> **Зауваження**
> 
> Існує можливість заборонити використання memcache як оброблювач сесій (session handler). Команда 'pecl install' видає про це запит (за замовчуванням увімкнено). Крім того, при статичній компіляції PHP для цієї мети можливе використання опції конфігурації **\-disable-memcache-session**
