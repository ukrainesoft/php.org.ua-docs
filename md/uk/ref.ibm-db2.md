---
navigation:
  - ibm-db2.constants.md: « Зумовлені константи
  - function.db2-autocommit.md: db2\_autocommit »
  - index.md: PHP Manual
  - book.ibm-db2.md: IBM DB2
title: Функції IBM DB2
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції IBM DB2

## Зміст

-   [db2\_autocommit](function.db2-autocommit.md)— Повертає або встановлює режим підтвердження транзакцій для з'єднання
-   [db2\_bind\_param](function.db2-bind-param.md)— Зв'язує змінну PHP із параметром SQL-виразу
-   [db2\_client\_info](function.db2-client-info.md)— Повертає об'єкт із властивостями, що описують клієнта DB2
-   [db2\_close](function.db2-close.md)— Закриває з'єднання з базою даних
-   [db2\_column\_privileges](function.db2-column-privileges.md)— Повертає результуючий набір, що перераховує стовпці та пов'язані з ним привілеї для таблиці
-   [db2\_columns](function.db2-columns.md)— Повертає результуючий набір, що перераховує стовпці та метадані для таблиці, пов'язані з ними.
-   [db2\_commit](function.db2-commit.md) \- Підтверджує транзакцію
-   [db2\_conn\_error](function.db2-conn-error.md)— Повертає рядок, який містить значення SQLSTATE, повернене останньою спробою підключення
-   [db2\_conn\_errormsg](function.db2-conn-errormsg.md)— Повертає останнє повідомлення про помилку підключення та значення SQLCODE
-   [db2\_connect](function.db2-connect.md)— Повертає з'єднання з базою даних
-   [db2\_cursor\_type](function.db2-cursor-type.md)— Повертає тип курсору, який використовується у ресурсі оператора
-   [db2\_escape\_string](function.db2-escape-string.md)— Використовується для екранування деяких символів
-   [db2\_exec](function.db2-exec.md)— Виконує SQL-запит безпосередньо
-   [db2\_execute](function.db2-execute.md) \- Виконує підготовлений SQL-запит
-   [db2\_fetch\_array](function.db2-fetch-array.md)— Повертає масив, індексований за положенням стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_assoc](function.db2-fetch-assoc.md)— Повертає масив, індексований на ім'я стовпця, який представляє рядок у наборі результатів
-   [db2\_fetch\_both](function.db2-fetch-both.md)— Повертає масив, індексований як на ім'я стовпця, так і на позицію, що представляє рядок у наборі результатів
-   [db2\_fetch\_object](function.db2-fetch-object.md)— Повертає об'єкт із властивостями, що становлять стовпці у вибраному рядку
-   [db2\_fetch\_row](function.db2-fetch-row.md)— Встановлює вказівник набору результатів на наступний рядок або запрошений рядок
-   [db2\_field\_display\_size](function.db2-field-display-size.md)— Повертає максимальну кількість байтів, необхідну для відображення стовпця
-   [db2\_field\_name](function.db2-field-name.md)— Повертає ім'я стовпця у наборі результатів
-   [db2\_field\_num](function.db2-field-num.md)— Повертає позицію зазначеного стовпця у наборі результатів
-   [db2\_field\_precision](function.db2-field-precision.md)— Повертає точність зазначеного стовпця у наборі результатів
-   [db2\_field\_scale](function.db2-field-scale.md)— Повертає масштаб вказаного стовпця у наборі результатів
-   [db2\_field\_type](function.db2-field-type.md)— Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2\_field\_width](function.db2-field-width.md)— Повертає ширину поточного значення вказаного стовпця у наборі результатів
-   [db2\_foreign\_keys](function.db2-foreign-keys.md)— Повертає набір результатів, де перелічені зовнішні ключі таблиці
-   [db2\_free\_result](function.db2-free-result.md)— Звільняє ресурси, пов'язані із набором результатів
-   [db2\_free\_stmt](function.db2-free-stmt.md)— Звільняє ресурси, пов'язані із зазначеним ресурсом вираження
-   [db2\_get\_option](function.db2-get-option.md)— Виймає параметр для ресурсу оператора або ресурсу з'єднання
-   [db2\_last\_insert\_id](function.db2-last-insert-id.md)— Повертає автоматично згенерований ідентифікатор останнього запиту додавання, успішно виконаного в цьому з'єднанні
-   [db2\_lob\_read](function.db2-lob-read.md)— Отримує певний користувач розмір LOB-файлів під час кожного виклику
-   [db2\_next\_result](function.db2-next-result.md)— Запитує наступний набір результатів із процедури, що зберігається.
-   [db2\_num\_fields](function.db2-num-fields.md)— Повертає кількість полів у результуючому наборі
-   [db2\_num\_rows](function.db2-num-rows.md)— Повертає кількість рядків, порушених SQL-запитом
-   [db2\_pclose](function.db2-pclose.md)— Закриває постійне з'єднання з базою даних
-   [db2\_pconnect](function.db2-pconnect.md)— Повертає постійне з'єднання з базою даних
-   [db2\_prepare](function.db2-prepare.md)— Підготовка SQL-запиту до виконання
-   [db2\_primary\_keys](function.db2-primary-keys.md)— Повертає набір результатів, що містить первинні ключі таблиці
-   [db2\_procedure\_columns](function.db2-procedure-columns.md)— Повертає набір результатів зі списком параметрів процедури, що зберігається.
-   [db2\_procedures](function.db2-procedures.md)— Повертає набір результатів, в якому перераховані процедури, що зберігаються, зареєстровані в базі даних
-   [db2\_result](function.db2-result.md)— Повертає один стовпець із рядка у наборі результатів
-   [db2\_rollback](function.db2-rollback.md) \- Відкочує транзакцію
-   [db2\_server\_info](function.db2-server-info.md)— Повертає об'єкт із властивостями, що описують сервер бази даних DB2
-   [db2\_set\_option](function.db2-set-option.md)— Встановити опцію для з'єднання або ресурсу оператора
-   [db2\_special\_columns](function.db2-special-columns.md)— Повертає набір результатів, у якому перераховані стовпці з унікальним ідентифікатором рядка таблиці
-   [db2\_statistics](function.db2-statistics.md)— Повертає набір результатів, що містить індекс та статистику таблиці
-   [db2\_stmt\_error](function.db2-stmt-error.md)— Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
-   [db2\_stmt\_errormsg](function.db2-stmt-errormsg.md)— Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу
-   [db2\_table\_privileges](function.db2-table-privileges.md)— Повертає набір результатів, у якому перелічені таблиці та пов'язані з ними права доступу до бази даних
-   [db2\_tables](function.db2-tables.md)— Повертає набір результатів, у якому перелічені таблиці та пов'язані метадані в базі даних
