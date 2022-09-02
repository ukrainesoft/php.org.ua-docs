---
navigation:
  - function.mysql-thread-id.md: « mysqlthreadід
  - book.mysqlnd.md: Mysqlnd »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlunbufferedquery
---
# mysqlunbufferedquery

(PHP 4> = 4.0.6, PHP 5)

mysqlunbufferedquery — Надсилає запит MySQL без авто-обробки результату та його буферизації

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   See: [Буферизовані та не буферизовані запити](mysqlinfo.concepts.buffering.md)

### Опис

```methodsynopsis
mysql_unbuffered_query(string $query, resource $link_identifier = NULL): resource
```

**mysqlunbufferedquery()** посилає запит MySQL `query` без автоматичної обробки та буферизації її результату, на відміну від функції [mysqlquery()](function.mysql-query.md). Це дозволяє зберегти досить велику кількість пам'яті для SQL-запитів, які повертають велику кількість даних. Крім того, ви можете почати роботу з отриманими даними відразу після того, як перший ряд був отриманий: вам не доводиться чекати до кінця SQL-запиту. При використанні **mysqlunbufferedquery()** з кількома з'єднаннями MySQL, ви повинні вказати необов'язковий параметр `link_identifier`

### Список параметрів

`query`

SQL-запит, що запускається.

Дані у запиті мають бути [коректно проекрановано](function.mysql-real-escape-string.md)

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Для SELECT, SHOW, DESCRIBE та EXPLAIN запитів **mysqlunbufferedquery()** повертає resource у разі успішного виконання, або **`false`** у разі виникнення помилки.

Для інших типів SQL-запитів, UPDATE, DELETE, DROP і т.д. **mysqlunbufferedquery()** повертає **`true`** у разі успіху та **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Однак, плюси використання **mysqlunbufferedquery()** мають свою ціну: ви не можете використовувати функції [mysqlnumrows()](function.mysql-num-rows.md) і [mysqldataseek()](function.mysql-data-seek.md) з результатом запиту, повернутим цією функцією, доки не будуть отримані всі ряди. Крім того, ви повинні будете обробити всі ряди запиту до відправки нового запиту, використовуючи той же `link_identifier`

### Дивіться також

-   [mysqlquery()](function.mysql-query.md) - Надсилає запит MySQL
