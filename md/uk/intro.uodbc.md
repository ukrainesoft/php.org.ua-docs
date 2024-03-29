---
navigation:
  - book.uodbc.md: « ODBC
  - uodbc.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.uodbc.md: ODBC
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

Крім звичайної підтримки ODBC, функції Unified ODBC в PHP дозволяють отримати доступ до кількох баз даних, які запозичили семантику ODBC API для реалізації свого власного API. Замість того, щоб підтримувати кілька драйверів баз даних, які були практично ідентичними, ці драйвери об'єднувалися в єдиний набір функцій ODBC.

Наступні бази даних підтримуються функціями Unified ODBC: [» Adabas D](http://www.adabas.com/) [» IBM DB2](http://www-306.ibm.com/software/data/db2/) [» iODBC](http://www.iodbc.org/) [» Solid](http://www.solidtech.com/), и[» Sybase SQL Anywhere](http://www.sybase.com/)

> **Зауваження** :
> 
> За винятком iODBC, при підключенні до вищевказаних баз даних ODBC не використовується. Функції, які ви використовуєте для безпосереднього спілкування з ними, мають ті самі імена і синтаксис, що і функції ODBC. Тим не менш, збірка PHP з підтримкою iODBC дозволяє вам використовувати будь-які ODBC-сумісні драйвери з вашими програмами PHP. Додаткову інформацію про iODBC можна отримати за адресою [» www.iodbc.org](http://www.iodbc.org/), а альтернативний варіант unixODBC доступний за адресою [» www.unixodbc.org](http://www.unixodbc.org/)
