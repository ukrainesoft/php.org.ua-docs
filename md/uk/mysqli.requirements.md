---
navigation:
  - mysqli.setup.md: '" Встановлення та налаштування'
  - mysqli.installation.md: Встановлення »
  - index.md: PHP Manual
  - mysqli.setup.md: Встановлення та налаштування
title: Вимоги
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вимоги

Ці функції доступні лише в PHP, який зібраний за допомогою модуля mysqli.

**MySQL 8**

При запуске PHP до версии 7.1.16, а также PHP с версии 7.2 до версии 7.2.4 в качестве плагина шифрования паролей по умолчанию для сервера MySQL 8 устанавливают*mysql\_native\_password*, інакше буде видана помилка на кшталт *The server requested authentication method unknown to the client\[caching\_sha2\_password\]*, даже когда плагин*caching\_sha2\_password*не задан.

Причина цього в тому, що на сервері MySQL 8 як плагін за замовчуванням вказано caching\_sha2\_password, який не розпізнається старими версіями PHP (модулем mysqlnd). Замість нього у файлі конфігурації сервера my.cnf вказують `default_authentication_plugin=mysql_native_password`Плагин*caching\_sha2\_password* отримав повну підтримку з PHP 7.4.4. У попередніх версіях PHP його підтримує модуль [mysql\_xdevapi](book.mysql-xdevapi.md)
