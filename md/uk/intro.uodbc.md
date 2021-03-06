- [«ODBC](book.uodbc.md)
- [Встановлення та налаштування »](uodbc.setup.md)

- [PHP Manual](index.md)
- [ODBC](book.uodbc.md)
-   Вступ

# Вступ

Крім звичайної підтримки ODBC, функції Unified ODBC в PHP
дозволяють отримати доступ до кількох баз даних, які
запозичили семантику ODBC API для реалізації свого власного
API. Замість підтримувати кілька драйверів баз даних,
які були практично ідентичні, ці драйвери були об'єднані в
єдиний набір функцій ODBC.

Наступні бази даних підтримуються функціями Unified ODBC: [» Adabas D](http://www.adabas.com/), [»IBM DB2](http://www-306.ibm.com/software/data/db2/),
[» iODBC](http://www.iodbc.org/), [»Solid](http://www.solidtech.com/),
та [» Sybase SQL Anywhere](http://www.sybase.com/).

> **Примітка**:
>
> За винятком iODBC, при підключенні до вищевказаних баз даних
> ODBC не використовується. Функції, які ви використовуєте для
> безпосереднього спілкування з ними, просто мають ті ж імена та
> синтаксис, як і функції ODBC. Тим не менш, складання PHP з підтримкою
> iODBC дозволяє вам використовувати будь-які ODBC-сумісні драйвери з
> вашими програмами PHP. Додаткову інформацію про iODBC можна
> отримати за адресою [»www.iodbc.org](http://www.iodbc.org/), а
> альтернативний варіант unixODBC доступний за адресою
> [» www.unixodbc.org](http://www.unixodbc.org/).
