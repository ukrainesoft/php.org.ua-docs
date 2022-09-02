---
navigation:
  - sqlsrv.constants.md: « Обумовлені константи
  - function.sqlsrv-begin-transaction.md: sqlsrvbegintransaction »
  - index.md: PHP Manual
  - book.sqlsrv.md: SQLSRV
title: Функції SQLSRV
---
# Функції SQLSRV

## Зміст

-   [sqlsrvbegintransaction](function.sqlsrv-begin-transaction.md) — Починає транзакцію бази даних
-   [sqlsrvcancel](function.sqlsrv-cancel.md) — скасовує оператор
-   [sqlsrvclientinfo](function.sqlsrv-client-info.md) — Повертає інформацію про клієнта та зазначене підключення
-   [sqlsrvclose](function.sqlsrv-close.md) — Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням.
-   [sqlsrvcommit](function.sqlsrv-commit.md) — Фіксує транзакцію, розпочату за допомогою sqlsrvbegintransaction
-   [sqlsrvconfigure](function.sqlsrv-configure.md) — Змінює конфігурацію обробки помилок драйвера та ведення журналу
-   [sqlsrvconnect](function.sqlsrv-connect.md) — Відкриває з'єднання з базою даних Microsoft SQL Server
-   [sqlsrverrors](function.sqlsrv-errors.md) — Повертає інформацію про помилку та попередження останньої виконаної операції SQLSRV
-   [sqlsrvexecute](function.sqlsrv-execute.md) — Виконує запит підготовлений за допомогою sqlsrvprepare
-   [sqlsrvfetcharray](function.sqlsrv-fetch-array.md) — Повертає рядок як масив
-   [sqlsrvfetchobject](function.sqlsrv-fetch-object.md) — Отримує наступний рядок даних у наборі результатів як об'єкт
-   [sqlsrvfetch](function.sqlsrv-fetch.md) — Робить наступний рядок у наборі результатів, доступних для читання.
-   [sqlsrvfieldmetadata](function.sqlsrv-field-metadata.md) — Отримує метадані для полів оператора, підготовленого за допомогою sqlsrvprepare або sqlsrvquery
-   [sqlsrvfreestmt](function.sqlsrv-free-stmt.md) — Звільняє всі ресурси для вказаного оператора
-   [sqlsrvgetconfig](function.sqlsrv-get-config.md) — Повертає значення вказаного параметра конфігурації
-   [sqlsrvgetfield](function.sqlsrv-get-field.md) — Отримує дані поля з поточного вибраного рядка
-   [sqlsrvhasrows](function.sqlsrv-has-rows.md) — Вказує, чи має зазначений оператор рядки
-   [sqlsrvnextresult](function.sqlsrv-next-result.md) — Робить активним наступний результат вказаного оператора
-   [sqlsrvnumfields](function.sqlsrv-num-fields.md) — Витягує кількість полів (стовпців) оператора
-   [sqlsrvnumrows](function.sqlsrv-num-rows.md) — Отримує кількість рядків у наборі результатів
-   [sqlsrvprepare](function.sqlsrv-prepare.md) — готує запит до виконання
-   [sqlsrvquery](function.sqlsrv-query.md) — готує та виконує запит
-   [sqlsrvrollback](function.sqlsrv-rollback.md) — Відкочує транзакцію, розпочату sqlsrvbegintransaction
-   [sqlsrvrowsaffected](function.sqlsrv-rows-affected.md) — Повертає кількість рядків, змінених останнім запитом INSERT, UPDATE або DELETE
-   [sqlsrvsendstreamdata](function.sqlsrv-send-stream-data.md) — Надсилає дані з потоків параметрів на сервер
-   [sqlsrvserverinfo](function.sqlsrv-server-info.md) — Повертає інформацію про сервер
