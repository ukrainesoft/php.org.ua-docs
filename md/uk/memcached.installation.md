---
navigation:
  - memcached.requirements.md: « Вимоги
  - memcached.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - memcached.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Встановлення PECL модулів](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/memcached](https://pecl.php.net/package/memcached)

Якщо libmemcached встановлена ​​в нестандартній директорії, використовуйте опцію **\--with-libmemcached-dir=DIR**, де DIR - це директорія, куди встановлено libmemcached. Ця директорія має містити файл include/libmemcached/memcached.h.

Библиотека Zlib необходима для поддержки сжатия. Для указания нестандартного расположения Zlib используйте ключ**\--with-zlib-dir=DIR**де DIR - це директорія установки Zlib.

Підтримка обробника сесій увімкнена за умовчанням. Для її вимкнення використовуйте ключ **\--disable-memcached-session**

Підтримка SASL автентифікації за замовчуванням вимкнена. Для її увімкнення використовуйте ключ **\--enable-memcached-sasl**. Для цього також потрібна встановлена ​​бібліотека libsasl2 і щоб libmemcached був зібраний із включеною підтримкою SASL.
