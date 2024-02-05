---
navigation:
  - function.cubrid-set-add.md: « cubrid\_set\_add
  - function.cubrid-set-db-parameter.md: cubrid\_set\_db\_parameter »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_set\_autocommit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_set\_autocommit

(PECL CUBRID >= 8.4.0)

cubrid\_set\_autocommit — Встановлює режим автокомміту для з'єднання.

### Опис

```methodsynopsis
cubrid_set_autocommit(resource $conn_identifier, bool $mode): bool
```

Функция\*\*cubrid\_set\_autocommit()\*\*используется для установки режима авто-коммита для соединения.

У CUBRID PHP, авто-коміт транзакцій за замовчуванням заборонено. Якщо ви увімкнете, всі очікувані транзакції будуть автоматично підтверджені.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`mode`

Режим авто-комміту. Одна з двох констант:

-   **`CUBRID_AUTOCOMMIT_FALSE`**
-   **`CUBRID_AUTOCOMMIT_TRUE`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [cubrid\_get\_autocommit()](function.cubrid-get-autocommit.md) \- Повертає налаштування авто-комміту для з'єднання
-   [cubrid\_commit()](function.cubrid-commit.md) \- підтвердження транзакції
