---
navigation:
  - ref.uodbc.md: « Функции ODBC
  - function.odbc-binmode.md: odbcbinmode »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcautocommit
---
# odbcautocommit

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcautocommit — Перемикає поведінку автоматичної фіксації

### Опис

```methodsynopsis
odbc_autocommit(resource $odbc, bool $enable = false): int|bool
```

Перемикає поведінку автоматичної фіксації.

За замовчуванням для підключення увімкнена автоматична фіксація. Вимкнення автоматичної фіксації еквівалентно запуску транзакції.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.md)

`enable`

Якщо `enable` встановлений **`true`**, автоматична фіксація включена, якщо **`false`** - автоматична фіксація вимкнена.

### Значення, що повертаються

Без параметра `enable` функція повертає статус автоматичної фіксації для `odbc`. Ненульове значення повертається, якщо автоматична фіксація увімкнена, 0 - якщо вимкнена та **`false`** у разі виникнення помилки.

Якщо встановлено значення `enable`, функція повертає **`true`** у разі успішного виконання та **`false`** у разі виникнення помилки.

### Дивіться також

-   [odbccommit()](function.odbc-commit.md) - Фіксує транзакцію ODBC
-   [odbcrollback()](function.odbc-rollback.md) - Відкочує транзакцію
