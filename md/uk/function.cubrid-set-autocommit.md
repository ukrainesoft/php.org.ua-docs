---
navigation:
  - function.cubrid-set-add.html: « cubridsetadd
  - function.cubrid-set-db-parameter.html: cubridsetдбparameter »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridsetautocommit
---
# cubridsetautocommit

(PECL CUBRID >= 8.4.0)

cubridsetautocommit — Встановлює режим автокомміту для з'єднання.

### Опис

```methodsynopsis
cubrid_set_autocommit(resource $conn_identifier, bool $mode): bool
```

Функція **cubridsetautocommit()** використовується для встановлення режиму автокомміту для з'єднання.

У CUBRID PHP, авто-коміт транзакцій за замовчуванням заборонено. Якщо ви увімкнете, всі очікувані транзакції будуть автоматично підтверджені.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`mode`

Режим авто-комміту. Одна з двох констант:

-   **`CUBRID_AUTOCOMMIT_FALSE`**
-   **`CUBRID_AUTOCOMMIT_TRUE`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubridgetautocommit()](function.cubrid-get-autocommit.html) - Повертає налаштування авто-комміту для з'єднання
-   [cubridcommit()](function.cubrid-commit.html) - підтвердження транзакції
