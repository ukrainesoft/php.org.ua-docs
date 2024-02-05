---
navigation:
  - rar.requirements.md: « Вимоги
  - rar.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - rar.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Модуль Rar в даний час доступний у PECL [» https://pecl.php.net/package/rar](https://pecl.php.net/package/rar)

Ви також можете скористатися інсталятором PECL, щоб встановити модуль Rar. Для цього необхідно використати команду: **pecl -v install rar**

Також ви можете завантажити архів tar.gz та встановити Rar вручну:

**Приклад #1 Установка Rar**

gunzip rar-xxx.tgz tar -xvf rar-xxx.tar cd rar-xxx phpize ./configure && make && make install

Користувачам Windows необхідно увімкнути php\_rar.dll у php.ini. DLL для цього модуля PECL поки що недоступна. Дивіться також розділ [збирання на Windows](install.windows.building.md)
