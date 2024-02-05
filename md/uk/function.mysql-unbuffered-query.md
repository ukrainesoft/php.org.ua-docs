---
navigation:
  - function.mysql-thread-id.md: « mysql\_thread\_id
  - book.mysqlnd.md: Mysqlnd »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_unbuffered\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_unbuffered\_query

(PHP 4 >= 4.0.6, PHP 5)

mysql\_unbuffered\_query — Надсилає запит MySQL без авто-обробки результату та його буферизації

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   See:[Буферизовані та не буферизовані запити](mysqlinfo.concepts.buffering.md)

### Опис

```methodsynopsis
mysql_unbuffered_query(string $query, resource $link_identifier = NULL): resource
```

**mysql\_unbuffered\_query()** посилає запит MySQL `query` без автоматичної обробки та буферизації її результату, на відміну від функції [mysql\_query()](function.mysql-query.md). Це дозволяє зберегти досить велику кількість пам'яті для SQL-запитів, які повертають велику кількість даних. Крім того, ви можете почати роботу з отриманими даними відразу після того, як перший ряд був отриманий: вам не доводиться чекати до кінця SQL-запиту. При використанні **mysql\_unbuffered\_query()** з кількома з'єднаннями MySQL, ви повинні вказати необов'язковий параметр `link_identifier`

### Список параметрів

`query`

SQL-запит, що запускається.

Дані у запиті мають бути [коректно проекрановано](function.mysql-real-escape-string.md)

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Для SELECT, SHOW, DESCRIBE та EXPLAIN запитів **mysql\_unbuffered\_query()** повертає resource у разі успішного виконання, або \*\*`false`\*\*в случае возникновения ошибки.

Для інших типів SQL-запитів, UPDATE, DELETE, DROP і т.д. **mysql\_unbuffered\_query()** повертає \*\*`true`**в случае успеха и**`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Однак, плюси використання **mysql\_unbuffered\_query()** мають свою ціну: ви не можете використовувати функції [mysql\_num\_rows()](function.mysql-num-rows.md) і [mysql\_data\_seek()](function.mysql-data-seek.md) з результатом запиту, повернутим цією функцією, доки не будуть отримані всі ряди. Крім того, ви повинні будете обробити всі ряди запиту до відправки нового запиту, використовуючи той же `link_identifier`

### Дивіться також

-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
