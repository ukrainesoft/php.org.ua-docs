---
navigation:
  - cubrid.examples.md: « Приклади
  - function.cubrid-bind.md: cubrid\_bind »
  - index.md: PHP Manual
  - book.cubrid.md: CUBRID
title: Функції CUBRID
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції CUBRID

## Зміст

-   [cubrid\_bind](function.cubrid-bind.md)— пов'язує змінні із підготовленим запитом
-   [cubrid\_close\_prepare](function.cubrid-close-prepare.md) \- Закриває обробник запиту
-   [cubrid\_close\_request](function.cubrid-close-request.md) \- Закриває обробник запиту
-   [cubrid\_col\_get](function.cubrid-col-get.md)— Отримання контенту стовпця типу колекція OID
-   [cubrid\_col\_size](function.cubrid-col-size.md)— Отримує кількість елементів у стовпці типу колекція OID
-   [cubrid\_column\_names](function.cubrid-column-names.md)— Отримати імена стовпців у результуючому наборі
-   [cubrid\_column\_types](function.cubrid-column-types.md)— Отримати типи стовпців у результуючому наборі
-   [cubrid\_commit](function.cubrid-commit.md) \- Підтвердження транзакції
-   [cubrid\_connect\_with\_url](function.cubrid-connect-with-url.md)— Створює оточення для з'єднання із сервером CUBRID
-   [cubrid\_connect](function.cubrid-connect.md)— Відкриває з'єднання з сервером CUBRID
-   [cubrid\_current\_oid](function.cubrid-current-oid.md)— Повертає OID поточної позиції курсору
-   [cubrid\_disconnect](function.cubrid-disconnect.md)— Закриває з'єднання з базою даних
-   [cubrid\_drop](function.cubrid-drop.md)— Видалення екземпляра OID
-   [cubrid\_error\_code\_facility](function.cubrid-error-code-facility.md)— Отримати код рівня, на якому сталася помилка
-   [cubrid\_error\_code](function.cubrid-error-code.md)— Отримати код помилки
-   [cubrid\_error\_msg](function.cubrid-error-msg.md)— Повертає текст останньої помилки, що сталася.
-   [cubrid\_execute](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
-   [cubrid\_fetch](function.cubrid-fetch.md)— Вибирає наступний рядок із набору результатів
-   [cubrid\_free\_result](function.cubrid-free-result.md) \- Звільняє пам'ять, зайняту даними результату
-   [cubrid\_get\_autocommit](function.cubrid-get-autocommit.md)— Повертає налаштування автокомміту для з'єднання
-   [cubrid\_get\_charset](function.cubrid-get-charset.md)— Повертає кодування поточного з'єднання CUBRID
-   [cubrid\_get\_class\_name](function.cubrid-get-class-name.md)— Отримує ім'я класу за допомогою OID
-   [cubrid\_get\_client\_info](function.cubrid-get-client-info.md)— Повертає версію клієнтської бібліотеки
-   [cubrid\_get\_db\_parameter](function.cubrid-get-db-parameter.md)— Повертає параметри бази даних CUBRID
-   [cubrid\_get\_query\_timeout](function.cubrid-get-query-timeout.md)— Отримує значення часу очікування запиту
-   [cubrid\_get\_server\_info](function.cubrid-get-server-info.md)— Повертає версію сервера CUBRID
-   [cubrid\_get](function.cubrid-get.md)— Отримує стовпець, використовуючи OID
-   [cubrid\_insert\_id](function.cubrid-insert-id.md)— Повертає ідентифікатор, згенерований для останнього оновленого стовпця AUTO\_INCREMENT
-   [cubrid\_is\_instance](function.cubrid-is-instance.md)— Перевіряє, чи існує екземпляр, на який вказує OID
-   [cubrid\_lob\_close](function.cubrid-lob-close.md)— Закриває дані BLOB/CLOB
-   [cubrid\_lob\_export](function.cubrid-lob-export.md)— Експортує дані BLOB/CLOB у файл
-   [cubrid\_lob\_get](function.cubrid-lob-get.md)— Отримує дані BLOB/CLOB
-   [cubrid\_lob\_send](function.cubrid-lob-send.md)— Читає дані BLOB/CLOB і надсилає їх прямо до браузера
-   [cubrid\_lob\_size](function.cubrid-lob-size.md)— Отримує розмір даних BLOB/CLOB
-   [cubrid\_lob2\_bind](function.cubrid-lob2-bind.md)— Зв'язує об'єкт LOB або рядок у вигляді об'єкта LOB з підготовленим оператором як параметри
-   [cubrid\_lob2\_close](function.cubrid-lob2-close.md)— Закриває об'єкт LOB
-   [cubrid\_lob2\_export](function.cubrid-lob2-export.md)— Експортує LOB-об'єкт у файл
-   [cubrid\_lob2\_import](function.cubrid-lob2-import.md)— Імпортує дані BLOB/CLOB із файлу
-   [cubrid\_lob2\_new](function.cubrid-lob2-new.md) \- Створює об'єкт LOB
-   [cubrid\_lob2\_read](function.cubrid-lob2-read.md)— Читає дані BLOB/CLOB
-   [cubrid\_lob2\_seek64](function.cubrid-lob2-seek64.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_seek](function.cubrid-lob2-seek.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_size64](function.cubrid-lob2-size64.md)— Отримує розмір LOB-об'єкта
-   [cubrid\_lob2\_size](function.cubrid-lob2-size.md)— Отримує розмір LOB-об'єкта
-   [cubrid\_lob2\_tell64](function.cubrid-lob2-tell64.md)— Повідомляє про положення курсора LOB-об'єкта
-   [cubrid\_lob2\_tell](function.cubrid-lob2-tell.md)— Повідомляє про положення курсора LOB-об'єкта
-   [cubrid\_lob2\_write](function.cubrid-lob2-write.md) \- Записує в LOB-об'єкт
-   [cubrid\_lock\_read](function.cubrid-lock-read.md)— Встановлює блокування читання для цього OID
-   [cubrid\_lock\_write](function.cubrid-lock-write.md)— Встановлює блокування запису для цього OID
-   [cubrid\_move\_cursor](function.cubrid-move-cursor.md)— Переміщує курсор у результаті
-   [cubrid\_next\_result](function.cubrid-next-result.md)— Отримує результат наступного запиту під час виконання кількох SQL-операторів
-   [cubrid\_num\_cols](function.cubrid-num-cols.md)— Повертає кількість стовпців у наборі результатів
-   [cubrid\_num\_rows](function.cubrid-num-rows.md)— Отримати кількість рядків у наборі результатів
-   [cubrid\_pconnect\_with\_url](function.cubrid-pconnect-with-url.md)— Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_pconnect](function.cubrid-pconnect.md)— Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_prepare](function.cubrid-prepare.md)— Підготовляє SQL-вираз до виконання
-   [cubrid\_put](function.cubrid-put.md)— Оновлює стовпець за допомогою OID
-   [cubrid\_rollback](function.cubrid-rollback.md) \- Відкат транзакції
-   [cubrid\_schema](function.cubrid-schema.md)— Отримує запитану інформацію про схему
-   [cubrid\_seq\_drop](function.cubrid-seq-drop.md)— Видаляє елемент зі стовпця типу послідовності, використовуючи OID
-   [cubrid\_seq\_insert](function.cubrid-seq-insert.md)— Вставляє елемент у стовпець типу послідовності, використовуючи OID
-   [cubrid\_seq\_put](function.cubrid-seq-put.md)— Оновлює значення елемента стовпця типу послідовності за допомогою OID
-   [cubrid\_set\_add](function.cubrid-set-add.md)— Вставляє один елемент для встановлення стовпця типу за допомогою OID
-   [cubrid\_set\_autocommit](function.cubrid-set-autocommit.md)— Встановлює режим автокомміту для з'єднання
-   [cubrid\_set\_db\_parameter](function.cubrid-set-db-parameter.md)— Встановлює параметри бази даних CUBRID
-   [cubrid\_set\_drop](function.cubrid-set-drop.md)— Видаляє елемент із стовпця заданого типу, використовуючи OID
-   [cubrid\_set\_query\_timeout](function.cubrid-set-query-timeout.md)— Встановлює час очікування на виконання запиту
-   [cubrid\_version](function.cubrid-version.md)— Отримати версію модуля CUBRID PHP
