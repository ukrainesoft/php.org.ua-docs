---
navigation:
  - sqlite3result.reset.md: '« SQLite3Result::reset'
  - intro.sqlsrv.md: Вступ "
  - index.md: PHP Manual
  - refs.database.vendors.md: Модулі для роботи з базами даних окремих виробників
title: Драйвер СУБД Microsoft SQL Server для PHP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Драйвер СУБД Microsoft SQL Server для PHP

-   [Вступ](intro.sqlsrv.md)
-   [Встановлення та налаштування](sqlsrv.setup.md)
    -   [Вимоги](sqlsrv.requirements.md)
    -   [Установка](sqlsrv.installation.md)
    -   [Налаштування під час виконання](sqlsrv.configuration.md)
    -   [Типи ресурсів](sqlsrv.resources.md)
-   [Обумовлені константи](sqlsrv.constants.md)
-   [Функції SQLSRV](ref.sqlsrv.md)
    -   [sqlsrv\_begin\_transaction](function.sqlsrv-begin-transaction.md)— Починає транзакцію бази даних
    -   [sqlsrv\_cancel](function.sqlsrv-cancel.md)— скасовує оператор
    -   [sqlsrv\_client\_info](function.sqlsrv-client-info.md)— Повертає інформацію про клієнта та зазначене підключення
    -   [sqlsrv\_close](function.sqlsrv-close.md)— Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням.
    -   [sqlsrv\_commit](function.sqlsrv-commit.md)— Фіксує транзакцію, розпочату за допомогою sqlsrv\_begin\_transaction
    -   [sqlsrv\_configure](function.sqlsrv-configure.md)— Змінює конфігурацію обробки помилок драйвера та ведення журналу
    -   [sqlsrv\_connect](function.sqlsrv-connect.md)— Відкриває з'єднання з базою даних Microsoft SQL Server
    -   [sqlsrv\_errors](function.sqlsrv-errors.md)— Повертає інформацію про помилку та попередження останньої виконаної операції SQLSRV
    -   [sqlsrv\_execute](function.sqlsrv-execute.md)— Виконує запит підготовлений за допомогою sqlsrv\_prepare
    -   [sqlsrv\_fetch\_array](function.sqlsrv-fetch-array.md)— Повертає рядок як масив
    -   [sqlsrv\_fetch\_object](function.sqlsrv-fetch-object.md)— Отримує наступний рядок даних у наборі результатів як об'єкт
    -   [sqlsrv\_fetch](function.sqlsrv-fetch.md)— Робить наступний рядок у наборі результатів, доступних для читання.
    -   [sqlsrv\_field\_metadata](function.sqlsrv-field-metadata.md)— Отримує метадані для полів оператора, підготовленого за допомогою sqlsrv\_prepare або sqlsrv\_query
    -   [sqlsrv\_free\_stmt](function.sqlsrv-free-stmt.md)— Звільняє всі ресурси для вказаного оператора
    -   [sqlsrv\_get\_config](function.sqlsrv-get-config.md)— Повертає значення вказаного параметра конфігурації
    -   [sqlsrv\_get\_field](function.sqlsrv-get-field.md)— Отримує дані поля з поточного вибраного рядка
    -   [sqlsrv\_has\_rows](function.sqlsrv-has-rows.md)— Вказує, чи має зазначений оператор рядки
    -   [sqlsrv\_next\_result](function.sqlsrv-next-result.md)— Робить активним наступний результат вказаного оператора
    -   [sqlsrv\_num\_fields](function.sqlsrv-num-fields.md)— Витягує кількість полів (стовпців) оператора
    -   [sqlsrv\_num\_rows](function.sqlsrv-num-rows.md)— Отримує кількість рядків у наборі результатів
    -   [sqlsrv\_prepare](function.sqlsrv-prepare.md)— готує запит до виконання
    -   [sqlsrv\_query](function.sqlsrv-query.md)— готує та виконує запит
    -   [sqlsrv\_rollback](function.sqlsrv-rollback.md)— Відкочує транзакцію, розпочату sqlsrv\_begin\_transaction
    -   [sqlsrv\_rows\_affected](function.sqlsrv-rows-affected.md)— Повертає кількість рядків, змінених останнім запитом INSERT, UPDATE або DELETE
    -   [sqlsrv\_send\_stream\_data](function.sqlsrv-send-stream-data.md)— Надсилає дані з потоків параметрів на сервер
    -   [sqlsrv\_server\_info](function.sqlsrv-server-info.md)— Повертає інформацію про сервер
