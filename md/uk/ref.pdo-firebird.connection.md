З'єднання з базою Firebird

-   [« Firebird (PDO)](ref.pdo-firebird.html)
    
-   [IBM (PDO) »](ref.pdo-ibm.html)
    
-   [PHP Manual](index.md)
    
-   [Firebird (PDO)](ref.pdo-firebird.html)
    
-   З'єднання з базою Firebird
    

# PDOFIREBIRD DSN

(PECL PDOFIREBIRD >= 0.1.0)

PDOFIREBIRD DSN — З'єднання з базою Firebird

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDOFIREBIRD складається з наступних елементів:

Префікс DSN

**`firebird:`**

`dbname`

Назва бази даних.

`charset`

Кодування.

`role`

Ім'я ролі SQL.

`dialect`

діалект бази даних; або `1` або `3`. Якщо не вказано, діалектом за замовчуванням буде `3`. Доступно з PHP 7.4.0.

### Приклади

**Приклад #1 Приклад PDOFIREBIRD DSN зі шляхом**

Наступний приклад демонструє PDOFIREBIRD DSN для з'єднання з базою Firebird:

```
firebird:dbname=/path/to/DATABASE.FDB
```

**Приклад #2 Приклад PDOFIREBIRD DSN з шляхом та портом**

Наступний приклад демонструє PDOFIREBIRD DSN із зазначенням шляху та порту для з'єднання з базою Firebird:

```
firebird:dbname=hostname/port:/path/to/DATABASE.FDB
```

**Приклад #3 Приклад PDOFIREBIRD DSN для localhost та шляхи до employee.fdb у системі Debian**

Наступний приклад демонструє PDOFIREBIRD DSN для з'єднання з Firebird на локальному хості та базою даних employee.fdb:

```
firebird:dbname=localhost:/var/lib/firebird/2.5/data/employee.fdb
```

**Приклад #4 PDOFIREBIRD DSN для підключення до dialect 1 database**

Наступний приклад демонструє PDOFIREBIRD DSN для з'єднання з базою даних Firebird test.fdb, яка була створена за допомогою діалекту 1. Підтримується починаючи з PHP 7.4.0.

```
firebird:dbname=localhost:/var/lib/firebird/2.5/data/test.fdb;charset=utf-8;dialect=1
```