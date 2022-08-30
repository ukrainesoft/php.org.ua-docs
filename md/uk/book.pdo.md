Об'єкти даних PHP

-   [« odbctables](function.odbc-tables.html)
    
-   [Введение »](intro.pdo.html)
    
-   [PHP Manual](index.html)
    
-   [Рівні абстракції](refs.database.abstract.html)
    
-   Об'єкти даних PHP
    

# Об'єкти даних PHP

-   [Введение](intro.pdo.html)
-   [Установка и настройка](pdo.setup.html)
    -   [Требования](pdo.requirements.html)
    -   [Установка](pdo.installation.html)
    -   [Настройка во время выполнения](pdo.configuration.html)
    -   [Типы ресурсов](pdo.resources.html)
-   [Предопределённые константы](pdo.constants.html)
-   [Подключения и управление подключениями](pdo.connections.html)
-   [Транзакції та автоматична фіксація змін](pdo.transactions.html)
-   [Підготовлені запити та процедури, що зберігаються](pdo.prepared-statements.html)
-   [Ошибки и их обработка](pdo.error-handling.html)
-   [Великі об'єкти (LOB)](pdo.lobs.html)
-   [PDO](class.pdo.html) - Клас PDO
    -   [PDO::beginTransaction](pdo.begintransaction.html) - Ініціалізація транзакції
    -   [PDO::commit](pdo.commit.html) - Фіксує транзакцію
    -   [PDO::construct](pdo.construct.html) — Створює екземпляр PDO, що надає з'єднання з базою даних
    -   [PDO::errorCode](pdo.errorcode.html) — Повертає код SQLSTATE результату останньої операції з базою даних
    -   [PDO::errorInfo](pdo.errorinfo.html) — Отримує розширену інформацію про помилку, що сталася під час останнього звернення до бази даних
    -   [PDO::exec](pdo.exec.html) — Виконує SQL-запит та повертає кількість порушених рядків
    -   [PDO::getAttribute](pdo.getattribute.html) — Отримати атрибут з'єднання з базою даних
    -   [PDO::getAvailableDrivers](pdo.getavailabledrivers.html) - Повертає масив доступних драйверів PDO
    -   [PDO::inTransaction](pdo.intransaction.html) — Перевіряє, чи розпочато транзакцію
    -   [PDO::lastInsertId](pdo.lastinsertid.html) — Повертає ID останнього вставленого рядка або значення послідовності
    -   [PDO::prepare](pdo.prepare.html) — готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
    -   [PDO::query](pdo.query.html) — Підготовляє та виконує вираз SQL без наповнювачів
    -   [PDO::quote](pdo.quote.html) — Укладає рядок у лапки для використання у запиті
    -   [PDO::rollBack](pdo.rollback.html) - Відкат транзакції
    -   [PDO::setAttribute](pdo.setattribute.html) - Встановлення атрибуту
-   [PDOStatement](class.pdostatement.html) - Клас PDOStatement
    -   [PDOStatement::bindColumn](pdostatement.bindcolumn.html) - Зв'язує стовпець зі змінною PHP
    -   [PDOStatement::bindParam](pdostatement.bindparam.html) — Прив'язує параметр запиту до змінної
    -   [PDOStatement::bindValue](pdostatement.bindvalue.html) — Зв'язує параметр із заданим значенням
    -   [PDOStatement::closeCursor](pdostatement.closecursor.html) — Закриває курсор, переводячи запит у стан готовності до повторного запуску
    -   [PDOStatement::columnCount](pdostatement.columncount.html) — Повертає кількість стовпців у результуючому наборі
    -   [PDOStatement::debugDumpParams](pdostatement.debugdumpparams.html) — Виведення інформації про підготовлену SQL-команду з метою налагодження
    -   [PDOStatement::errorCode](pdostatement.errorcode.html) — Отримує код SQLSTATE, пов'язаний із останньою операцією в об'єкті PDOStatement
    -   [PDOStatement::errorInfo](pdostatement.errorinfo.html) — Отримання розширеної інформації про помилку, що сталася внаслідок роботи об'єкта PDOStatement
    -   [PDOStatement::execute](pdostatement.execute.html) - Запускає підготовлений запит на виконання
    -   [PDOStatement::fetch](pdostatement.fetch.html) — Витяг наступного рядка з результуючого набору
    -   [PDOStatement::fetchAll](pdostatement.fetchall.html) — Вибирає рядки, що залишилися, з набору результатів
    -   [PDOStatement::fetchColumn](pdostatement.fetchcolumn.html) — Повертає дані одного стовпця наступного рядка результуючого набору
    -   [PDOStatement::fetchObject](pdostatement.fetchobject.html) — Витягує наступний рядок і повертає його у вигляді об'єкта
    -   [PDOStatement::getAttribute](pdostatement.getattribute.html) — Отримання атрибуту запиту PDOStatement
    -   [PDOStatement::getColumnMeta](pdostatement.getcolumnmeta.html) — Повертає метадані стовпця у результуючій таблиці
    -   [PDOStatement::getIterator](pdostatement.getiterator.html) — Отримує ітератор набору результатів
    -   [PDOStatement::nextRowset](pdostatement.nextrowset.html) — Перехід до наступного набору рядків через запит
    -   [PDOStatement::rowCount](pdostatement.rowcount.html) — Повертає кількість рядків, порушених останнім SQL-запитом
    -   [PDOStatement::setAttribute](pdostatement.setattribute.html) — Встановлює атрибут об'єкту PDOStatement
    -   [PDOStatement::setFetchMode](pdostatement.setfetchmode.html) — Встановлює стандартний режим вибірки для об'єкта запиту
-   [PDOException](class.pdoexception.html) - Клас PDOException
-   [Драйвери PDO](pdo.drivers.html)
    -   [CUBRID (PDO)](ref.pdo-cubrid.html) - Функції CUBRID (PDOCUBRID)
    -   [MS SQL Server (PDODBLIB)](ref.pdo-dblib.html) — Функції Microsoft SQL Server та Sybase (PDODBLIB)
    -   [Firebird (PDO)](ref.pdo-firebird.html) - Функції Firebird (PDOFIREBIRD)
    -   [IBM (PDO)](ref.pdo-ibm.html) - Функції IBM (PDOIBM)
    -   [Informix (PDO)](ref.pdo-informix.html) - Функції Informix (PDOINFORMIX)
    -   [MySQL (PDO)](ref.pdo-mysql.html) - Функції MySQL (PDOMYSQL)
    -   [MS SQL Server (PDO)](ref.pdo-sqlsrv.html) - Функції модуля PDOSQLSRV для Microsoft SQL Server
    -   [Oracle (PDO)](ref.pdo-oci.html) - Функції Oracle (PDOOCI)
    -   [ODBC и DB2 (PDO)](ref.pdo-odbc.html) — Функції ODBC та DB2 (PDOODBC)
    -   [PostgreSQL (PDO)](ref.pdo-pgsql.html) - Функції PostgreSQL (PDOPGSQL)
    -   [SQLite (PDO)](ref.pdo-sqlite.html) - Функції SQLite (PDOSQLITE)