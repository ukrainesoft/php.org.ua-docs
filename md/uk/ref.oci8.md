OCI8 Функції

-   [« Поддерживаемые типы данных](oci8.datatypes.html)
    
-   [oci\_bind\_array\_by\_name »](function.oci-bind-array-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8](book.oci8.html)
    
-   OCI8 Функції
    

# OCI8 Функції

## Зміст

-   [oci\_bind\_array\_by\_name](function.oci-bind-array-by-name.html) — Пов'язує PHP масив з масивом Oracle PL/SQL
-   [oci\_bind\_by\_name](function.oci-bind-by-name.html) — Прикріплює змінну PHP до відповідної мітки у SQL-вираженні
-   [oci\_cancel](function.oci-cancel.html) - Закінчує процес читання з курсору
-   [oci\_client\_version](function.oci-client-version.html) — Повертає версію клієнтської бібліотеки
-   [oci\_close](function.oci-close.html) — Закриває з'єднання із сервером Oracle
-   [oci\_commit](function.oci-commit.html) - Підтверджує транзакцію бази даних
-   [oci\_connect](function.oci-connect.html) — Встановлює з'єднання з базою даних Oracle
-   [oci\_define\_by\_name](function.oci-define-by-name.html) — Порівнює змінну PHP стовпцю результату запиту
-   [oci\_error](function.oci-error.html) — Повертає останню помилку
-   [oci\_execute](function.oci-execute.html) — Виконує підготовлений вираз
-   [oci\_fetch\_all](function.oci-fetch-all.html) — Вибирає всі рядки з результату запиту до двовимірного масиву
-   [oci\_fetch\_array](function.oci-fetch-array.html) — Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_assoc](function.oci-fetch-assoc.html) — Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_object](function.oci-fetch-object.html) — Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [oci\_fetch\_row](function.oci-fetch-row.html) — Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [oci\_fetch](function.oci-fetch.html) — Вибирає наступний рядок із результату до буфера
-   [oci\_field\_is\_null](function.oci-field-is-null.html) — Перевіряє, чи поле в поточному отриманому ряду дорівнює null
-   [oci\_field\_name](function.oci-field-name.html) — Повертає ім'я поля із результату запиту
-   [oci\_field\_precision](function.oci-field-precision.html) — Повертає точність поля
-   [oci\_field\_scale](function.oci-field-scale.html) — Повертає масштаб поля
-   [oci\_field\_size](function.oci-field-size.html) — Повертає розмір поля
-   [oci\_field\_type\_raw](function.oci-field-type-raw.html) — Повертає вихідний тип поля Oracle
-   [oci\_field\_type](function.oci-field-type.html) - Повертає ім'я типу поля
-   [oci\_free\_descriptor](function.oci-free-descriptor.html) - Звільняє дескриптор
-   [oci\_free\_statement](function.oci-free-statement.html) — Звільняє ресурси, які займає курсор або SQL-вираз.
-   [oci\_get\_implicit\_resultset](function.oci-get-implicit-resultset.html) — Повертає наступний ресурс дочірнього запиту з батьківського запиту, що має неявні результуючі набори Oracle Database
-   [oci\_lob\_copy](function.oci-lob-copy.html) - Копіює об'єкт LOB
-   [oci\_lob\_is\_equal](function.oci-lob-is-equal.html) — Порівнює два об'єкти LOB/FILE
-   [oci\_new\_collection](function.oci-new-collection.html) — Створює новий об'єкт колекції
-   [oci\_new\_connect](function.oci-new-connect.html) — Встановлює нове з'єднання із сервером Oracle
-   [oci\_new\_cursor](function.oci-new-cursor.html) - Повертає ідентифікатор створеного курсору
-   [oci\_new\_descriptor](function.oci-new-descriptor.html) - Ініціалізує новий дескриптор об'єкта LOB або FILE
-   [oci\_num\_fields](function.oci-num-fields.html) — Повертає кількість полів через запит
-   [oci\_num\_rows](function.oci-num-rows.html) — Повертає кількість рядків, змінених у процесі виконання запиту
-   [oci\_parse](function.oci-parse.html) — готує запит до виконання
-   [oci\_password\_change](function.oci-password-change.html) — Змінює пароль користувача Oracle
-   [oci\_pconnect](function.oci-pconnect.html) — Встановлює постійне з'єднання із сервером Oracle
-   [oci\_register\_taf\_callback](function.oci-register-taf-callback.html) — Реєструє функцію зворотного виклику для Oracle Database TAF
-   [oci\_result](function.oci-result.html) — Повертає значення поля із результату запиту
-   [oci\_rollback](function.oci-rollback.html) — Відкочує транзакції, які очікують на обробку
-   [oci\_server\_version](function.oci-server-version.html) — Повертає версію сервера Oracle
-   [oci\_set\_action](function.oci-set-action.html) — Вказує ім'я для дії
-   [oci\_set\_call\_timeout](function.oci-set-call-timout.html) — Встановлює час очікування у мілісекундах для викликів бази даних
-   [oci\_set\_client\_identifier](function.oci-set-client-identifier.html) - Задає ідентифікатор клієнта
-   [oci\_set\_client\_info](function.oci-set-client-info.html) - Задає інформацію про клієнта
-   [oci\_set\_db\_operation](function.oci-set-db-operation.html) — Задає операцію бази даних
-   [oci\_set\_edition](function.oci-set-edition.html) - Задає випуск (edition) бази даних
-   [oci\_set\_module\_name](function.oci-set-module-name.html) - Задає ім'я модулю
-   [oci\_set\_prefetch\_lob](function.oci-set-prefetch-lob.html) — Встановлює обсяг даних, що попередньо вибираються для кожного CLOB або BLOB
-   [oci\_set\_prefetch](function.oci-set-prefetch.html) — Встановлює кількість рядків, які будуть автоматично вибрані в буфер
-   [oci\_statement\_type](function.oci-statement-type.html) — Повертає тип виразу
-   [oci\_unregister\_taf\_callback](function.oci-unregister-taf-callback.html) — Видалити реєстрацію користувача callback-функції для Oracle Database TAF