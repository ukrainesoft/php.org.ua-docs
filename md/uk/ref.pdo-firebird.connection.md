---
navigation:
  - ref.pdo-firebird.md: « Firebird (PDO)
  - ref.pdo-ibm.md: IBM (PDO) »
  - index.md: PHP Manual
  - ref.pdo-firebird.md: Firebird (PDO)
title: PDO\_FIREBIRD DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_FIREBIRD DSN

(PECL PDO\_FIREBIRD >= 0.1.0)

PDO\_FIREBIRD DSN — З'єднання з базою Firebird

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDO\_FIREBIRD складається з наступних елементів:

Префікс DSN

**`firebird:`**

`dbname`

Назва бази даних.

`charset`

Кодування.

`role`

Ім'я ролі SQL.

`dialect`

діалект бази даних; або или`3`. Якщо не вказано, діалектом за замовчуванням буде `3`Доступно с PHP 7.4.0.

### Приклади

**Приклад #1 Приклад PDO\_FIREBIRD DSN зі шляхом**

Наступний приклад демонструє PDO\_FIREBIRD DSN для з'єднання з базою Firebird:

```
firebird:dbname=/path/to/DATABASE.FDB
```

**Приклад #2 Приклад PDO\_FIREBIRD DSN з шляхом та портом**

Наступний приклад демонструє PDO\_FIREBIRD DSN із зазначенням шляху та порту для з'єднання з базою Firebird:

```
firebird:dbname=hostname/port:/path/to/DATABASE.FDB
```

**Приклад #3 Приклад PDO\_FIREBIRD DSN для localhost та шляхи до employee.fdb у системі Debian**

Наступний приклад демонструє PDO\_FIREBIRD DSN для з'єднання з Firebird на локальному хості та базою даних employee.fdb:

```
firebird:dbname=localhost:/var/lib/firebird/2.5/data/employee.fdb
```

**Приклад #4 PDO\_FIREBIRD DSN to connect to a dialect 1 database**

Наступний приклад демонструє PDO\_FIREBIRD DSN для з'єднання з базою даних Firebird test.fdb, яка була створена за допомогою діалекту 1. Підтримується починаючи з PHP 7.4.0.

```
firebird:dbname=localhost:/var/lib/firebird/2.5/data/test.fdb;charset=utf-8;dialect=1
```
