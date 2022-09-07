---
navigation:
  - mysqli.setup.md: « Встановлення та налаштування
  - mysqli.installation.md: Установка »
  - index.md: PHP Manual
  - mysqli.setup.md: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Щоб ці функції були доступні, PHP має бути зібраний за допомогою модуля mysqli.

*MySQL 8*

При запуску PHP до версії 7.1.16 або PHP 7.2 до 7.2.4 встановіть плагін за умовчанням MySQL 8 Server в *mysqlnativepassword*, інакше ви побачите помилки, схожі на *Server потребує authentication method unknown to the client cachingsha2password*, навіть коли *cachingsha2password* не використовується.

Це пов'язано з тим, що MySQL 8 за замовчуванням використовує cachingsha2password, і плагін не розпізнається старими версіями PHP (mysqlnd). Натомість змініть це, встановивши `default_authentication_plugin=mysql_native_password` у my.cnf. Плагін *cachingsha2password* буде підтримуватись у майбутній версії PHP. Поки що модуль [mysqlxdevapi](book.mysql-xdevapi.md) підтримує його.
