---
navigation:
  - oci8.datatypes.md: '« Типи даних, що підтримуються'
  - function.oci-bind-array-by-name.md: oci\_bind\_array\_by\_name »
  - index.md: PHP Manual
  - book.oci8.md: OCI8
title: OCI8 Функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCI8 Функції

## Зміст

-   [oci\_bind\_array\_by\_name](function.oci-bind-array-by-name.md)— Пов'язує PHP масив з масивом Oracle PL/SQL
-   [oci\_bind\_by\_name](function.oci-bind-by-name.md)— Прикріплює змінну PHP до відповідної мітки у SQL-вираженні
-   [oci\_cancel](function.oci-cancel.md) \- Закінчує процес читання з курсору
-   [oci\_client\_version](function.oci-client-version.md)— Повертає версію клієнтської бібліотеки
-   [oci\_close](function.oci-close.md)— Закриває з'єднання із сервером Oracle
-   [oci\_commit](function.oci-commit.md) \- Підтверджує транзакцію бази даних
-   [oci\_connect](function.oci-connect.md)— Встановлює з'єднання з базою даних Oracle
-   [oci\_define\_by\_name](function.oci-define-by-name.md)— Порівнює змінну PHP стовпцю результату запиту
-   [oci\_error](function.oci-error.md)— Повертає останню помилку
-   [oci\_execute](function.oci-execute.md)— Виконує підготовлений вираз
-   [oci\_fetch\_all](function.oci-fetch-all.md)— Вибирає всі рядки з результату запиту до двовимірного масиву
-   [oci\_fetch\_array](function.oci-fetch-array.md)— Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_assoc](function.oci-fetch-assoc.md)— Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_object](function.oci-fetch-object.md)— Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [oci\_fetch\_row](function.oci-fetch-row.md)— Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [oci\_fetch](function.oci-fetch.md)— Вибирає наступний рядок із результату до буфера
-   [oci\_field\_is\_null](function.oci-field-is-null.md)— Перевіряє, чи поле в поточному отриманому ряду дорівнює null
-   [oci\_field\_name](function.oci-field-name.md)— Повертає ім'я поля із результату запиту
-   [oci\_field\_precision](function.oci-field-precision.md)— Повертає точність поля
-   [oci\_field\_scale](function.oci-field-scale.md)— Повертає масштаб поля
-   [oci\_field\_size](function.oci-field-size.md)— Повертає розмір поля
-   [oci\_field\_type\_raw](function.oci-field-type-raw.md)— Повертає вихідний тип поля Oracle
-   [oci\_field\_type](function.oci-field-type.md) \- Повертає ім'я типу поля
-   [oci\_free\_descriptor](function.oci-free-descriptor.md) \- Звільняє дескриптор
-   [oci\_free\_statement](function.oci-free-statement.md)— Звільняє ресурси, які займає курсор або SQL-вираз.
-   [oci\_get\_implicit\_resultset](function.oci-get-implicit-resultset.md)— Повертає наступний ресурс дочірнього запиту з батьківського запиту, що має неявні результуючі набори Oracle Database
-   [oci\_lob\_copy](function.oci-lob-copy.md) \- Копіює об'єкт LOB
-   [oci\_lob\_is\_equal](function.oci-lob-is-equal.md)— Порівнює два об'єкти LOB/FILE
-   [oci\_new\_collection](function.oci-new-collection.md)— Створює новий об'єкт колекції
-   [oci\_new\_connect](function.oci-new-connect.md)— Встановлює нове з'єднання із сервером Oracle
-   [oci\_new\_cursor](function.oci-new-cursor.md)— Повертає ідентифікатор створеного курсору
-   [oci\_new\_descriptor](function.oci-new-descriptor.md) \- Ініціалізує новий дескриптор об'єкта LOB або FILE
-   [oci\_num\_fields](function.oci-num-fields.md)— Повертає кількість полів через запит
-   [oci\_num\_rows](function.oci-num-rows.md)— Повертає кількість рядків, змінених у процесі виконання запиту
-   [oci\_parse](function.oci-parse.md)— готує запит до виконання
-   [oci\_password\_change](function.oci-password-change.md)— Змінює пароль користувача Oracle
-   [oci\_pconnect](function.oci-pconnect.md)— Встановлює постійне з'єднання із сервером Oracle
-   [oci\_register\_taf\_callback](function.oci-register-taf-callback.md)— Реєструє функцію зворотного виклику для Oracle Database TAF
-   [oci\_result](function.oci-result.md)— Повертає значення поля із результату запиту
-   [oci\_rollback](function.oci-rollback.md)— Відкочує транзакції, які очікують на обробку
-   [oci\_server\_version](function.oci-server-version.md)— Повертає версію сервера Oracle
-   [oci\_set\_action](function.oci-set-action.md)— Вказує ім'я для дії
-   [oci\_set\_call\_timeout](function.oci-set-call-timout.md)— Встановлює час очікування у мілісекундах для викликів бази даних
-   [oci\_set\_client\_identifier](function.oci-set-client-identifier.md) \- Задає ідентифікатор клієнта
-   [oci\_set\_client\_info](function.oci-set-client-info.md) \- Задає інформацію про клієнта
-   [oci\_set\_db\_operation](function.oci-set-db-operation.md)— Задає операцію бази даних
-   [oci\_set\_edition](function.oci-set-edition.md) \- Задає випуск (edition) бази даних
-   [oci\_set\_module\_name](function.oci-set-module-name.md) \- Задає ім'я модулю
-   [oci\_set\_prefetch\_lob](function.oci-set-prefetch-lob.md)— Встановлює обсяг даних, що попередньо вибираються для кожного CLOB або BLOB
-   [oci\_set\_prefetch](function.oci-set-prefetch.md)— Встановлює кількість рядків, які будуть автоматично вибрані в буфер
-   [oci\_statement\_type](function.oci-statement-type.md)— Повертає тип виразу
-   [oci\_unregister\_taf\_callback](function.oci-unregister-taf-callback.md)— Видалити реєстрацію користувача callback-функції для Oracle Database TAF
