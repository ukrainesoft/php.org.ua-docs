---
navigation:
  - sodium.requirements.md: « Вимоги
  - sodium.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - sodium.setup.md: Встановлення та налаштування
title: Встановлення
---
## Встановлення

Починаючи з PHP 7.2.0, модуль включено до PHP. Для старіших версій PHP модуль доступний через PECL.

## Linux Systems

Для того, щоб використовувати модуль, вам потрібно скомпілювати PHP за допомогою sodium, використовуючи конфігураційну опцію **\-with-sodium=DIR**

## Windows

Для того щоб використовувати модуль, вам потрібно додати `extension=php_sodium.dll` у файл php.ini.

## Установка через PECL

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Установка PECL модулей](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/libsodium](https://pecl.php.net/package/libsodium)
