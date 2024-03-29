---
navigation:
  - function.dba-sync.md: « dba\_sync
  - intro.uodbc.md: Вступ "
  - index.md: PHP Manual
  - refs.database.abstract.md: Рівні абстракції
title: ODBC (Unified)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ODBC (Unified)

-   [Вступ](intro.uodbc.md)
-   [Встановлення та налаштування](uodbc.setup.md)
    -   [Вимоги](uodbc.requirements.md)
    -   [Установка](odbc.installation.md)
    -   [Налаштування під час виконання](odbc.configuration.md)
    -   [Типи ресурсів](uodbc.resources.md)
-   [Обумовлені константи](uodbc.constants.md)
-   [Функції ODBC](ref.uodbc.md)
    -   [odbc\_autocommit](function.odbc-autocommit.md)— Перемикає поведінку автоматичної фіксації
    -   [odbc\_binmode](function.odbc-binmode.md)— керує обробкою двійкових даних стовпця
    -   [odbc\_close\_all](function.odbc-close-all.md)— Закриває всі з'єднання ODBC
    -   [odbc\_close](function.odbc-close.md)— Закриває з'єднання ODBC
    -   [odbc\_columnprivileges](function.odbc-columnprivileges.md)— Перераховує стовпці та пов'язані привілеї для даної таблиці
    -   [odbc\_columns](function.odbc-columns.md)— Перераховує імена стовпців у зазначених таблицях
    -   [odbc\_commit](function.odbc-commit.md) \- Фіксує транзакцію ODBC
    -   [odbc\_connect](function.odbc-connect.md)— З'єднує із джерелом даних
    -   [odbc\_connection\_string\_is\_quoted](function.odbc-connection-string-is-quoted.md)— Визначає, чи встановлено значення рядка з'єднання ODBC у лапки.
    -   [odbc\_connection\_string\_quote](function.odbc-connection-string-quote.md)— Укладає в лапки значення рядка підключення
    -   [odbc\_connection\_string\_should\_quote](function.odbc-connection-string-should-quote.md)— Визначає, чи слід укладати значення рядка з'єднання ODBC у лапки
    -   [odbc\_cursor](function.odbc-cursor.md) \- Повертає ім'я курсора
    -   [odbc\_data\_source](function.odbc-data-source.md)— Повертає інформацію про доступні DSN
    -   [odbc\_do](function.odbc-do.md) \- Псевдонім odbc\_exec
    -   [odbc\_error](function.odbc-error.md)— Повертає останній код помилки
    -   [odbc\_errormsg](function.odbc-errormsg.md)— Повертає останнє повідомлення про помилку
    -   [odbc\_exec](function.odbc-exec.md)— Виконує інструкцію SQL безпосередньо
    -   [odbc\_execute](function.odbc-execute.md)— Виконує запит
    -   [odbc\_fetch\_array](function.odbc-fetch-array.md)— Повертає рядок результату у вигляді асоціативного масиву
    -   [odbc\_fetch\_into](function.odbc-fetch-into.md)— Повертає один рядок результату до масиву
    -   [odbc\_fetch\_object](function.odbc-fetch-object.md)— Повертає рядок результату як об'єкт
    -   [odbc\_fetch\_row](function.odbc-fetch-row.md)— Повертає рядок
    -   [odbc\_field\_len](function.odbc-field-len.md) \- Повертає довжину (точність) поля
    -   [odbc\_field\_name](function.odbc-field-name.md)— Повертає ім'я стовпця
    -   [odbc\_field\_num](function.odbc-field-num.md) \- Повертає номер стовпця
    -   [odbc\_field\_precision](function.odbc-field-precision.md) \- Псевдонім odbc\_field\_len
    -   [odbc\_field\_scale](function.odbc-field-scale.md)— Повертає масштаб поля
    -   [odbc\_field\_type](function.odbc-field-type.md)— Повертає тип даних поля
    -   [odbc\_foreignkeys](function.odbc-foreignkeys.md)— Повертає список зовнішніх ключів
    -   [odbc\_free\_result](function.odbc-free-result.md) \- Звільняє ресурси, пов'язані з результатом
    -   [odbc\_gettypeinfo](function.odbc-gettypeinfo.md)— Повертає інформацію про типи даних, що підтримуються джерелом даних
    -   [odbc\_longreadlen](function.odbc-longreadlen.md) \- Обробляє стовпці LONG
    -   [odbc\_next\_result](function.odbc-next-result.md)— Перевіряє, чи є кілька результатів.
    -   [odbc\_num\_fields](function.odbc-num-fields.md)— Повертає кількість стовпців у результаті
    -   [odbc\_num\_rows](function.odbc-num-rows.md)— Повертає кількість рядків у результаті
    -   [odbc\_pconnect](function.odbc-pconnect.md)— Відкриває постійне з'єднання з базою даних
    -   [odbc\_prepare](function.odbc-prepare.md)— готує запит до виконання
    -   [odbc\_primarykeys](function.odbc-primarykeys.md)— Отримує первинні ключі таблиці
    -   [odbc\_procedurecolumns](function.odbc-procedurecolumns.md)— Отримує інформацію про параметри процедур
    -   [odbc\_procedures](function.odbc-procedures.md)— Отримує список процедур, що зберігаються у певному джерелі даних
    -   [odbc\_result\_all](function.odbc-result-all.md) \- Виводить результат у вигляді HTML-таблиці
    -   [odbc\_result](function.odbc-result.md)— Отримує дані результату
    -   [odbc\_rollback](function.odbc-rollback.md) \- Відкочує транзакцію
    -   [odbc\_setoption](function.odbc-setoption.md)— Регулює налаштування ODBC
    -   [odbc\_specialcolumns](function.odbc-specialcolumns.md)— Витягує спеціальні стовпці
    -   [odbc\_statistics](function.odbc-statistics.md)— Отримує статистику про таблицю
    -   [odbc\_tableprivileges](function.odbc-tableprivileges.md)— Перелічує таблиці та привілеї, пов'язані з кожною таблицею
    -   [odbc\_tables](function.odbc-tables.md)— Отримує список імен таблиць, що зберігаються у певному джерелі даних
