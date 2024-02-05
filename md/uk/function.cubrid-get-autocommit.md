---
navigation:
  - function.cubrid-free-result.md: « cubrid\_free\_result
  - function.cubrid-get-charset.md: cubrid\_get\_charset »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_get\_autocommit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_get\_autocommit

(PECL CUBRID >= 8.4.0)

cubrid\_get\_autocommit — Повертає налаштування автокомміту для з'єднання

### Опис

```methodsynopsis
cubrid_get_autocommit(resource $conn_identifier): bool
```

Функция**cubrid\_get\_autocommit()** використовується для визначення, чи дозволено в цьому з'єднанні авто-комміт чи ні.

Для CUBRID 8.4.0, авто-коміт транзакцій заборонено за замовчуванням.

Для CUBRID 8.4.0, авто-коміт транзакцій дозволено за замовчуванням.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

### Значення, що повертаються

**`true`**, якщо автокоміт дозволено.

**`false`**, якщо автокоміт заборонено.

\*\*`null`\*\*в случае возникновения ошибки.

### Дивіться також

-   [cubrid\_set\_autocommit()](function.cubrid-set-autocommit.md) \- Встановлює режим авто-комміту для з'єднання
-   [cubrid\_commit()](function.cubrid-commit.md) \- підтвердження транзакції
