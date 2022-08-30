SQLite3

-   [« PgSqlLob](class.pgsql-lob.html)
    
-   [Введение »](intro.sqlite3.html)
    
-   [PHP Manual](index.html)
    
-   [Модулі для роботи з базами даних окремих виробників](refs.database.vendors.html)
    
-   SQLite3
    

# SQLite3

-   [Введение](intro.sqlite3.html)
-   [Встановлення та налаштування](sqlite3.setup.html)
    -   [Вимоги](sqlite3.requirements.html)
    -   [Установка](sqlite3.installation.html)
    -   [Налаштування під час виконання](sqlite3.configuration.html)
    -   [Типи ресурсів](sqlite3.resources.html)
-   [Обумовлені константи](sqlite3.constants.html)
-   [SQLite3](class.sqlite3.html) - Клас SQLite3
    -   [SQLite3::backup](sqlite3.backup.html) — Резервне копіювання однієї бази даних до іншої
    -   [SQLite3::busyTimeout](sqlite3.busytimeout.html) - Встановити обробник "зайнято" на з'єднання
    -   [SQLite3::changes](sqlite3.changes.html) — Отримати кількість рядків, які були змінені/віддалені/вставлені останнім запитом
    -   [SQLite3::close](sqlite3.close.html) — Закрити з'єднання з базою даних
    -   [SQLite3::construct](sqlite3.construct.html) — Створює екземпляр SQLite3 і відкриває з'єднання з базою
    -   [SQLite3::createAggregate](sqlite3.createaggregate.html) — Зареєструвати функцію PHP як агрегуючу функцію SQL
    -   [SQLite3::createCollation](sqlite3.createcollation.html) — Реєструє функцію PHP для використання як функцію сортування SQL
    -   [SQLite3::createFunction](sqlite3.createfunction.html) — Реєструє функцію PHP для використання як скалярну функцію SQL
    -   [SQLite3::enableExceptions](sqlite3.enableexceptions.html) - Включити викид винятків
    -   [SQLite3::escapeString](sqlite3.escapestring.html) — Повертає правильно екранований рядок
    -   [SQLite3::exec](sqlite3.exec.html) — Виконує запит без результату до поточної бази даних
    -   [SQLite3::lastErrorCode](sqlite3.lasterrorcode.html) — Повертає числовий код результату останнього невдалого запиту SQLite
    -   [SQLite3::lastErrorMsg](sqlite3.lasterrormsg.html) — Повертає текст англійською, що описує останній невдалий запит SQLite
    -   [SQLite3::lastInsertRowID](sqlite3.lastinsertrowid.html) — Повертає ідентифікатор рядка останньої вставки (INSERT) до бази даних
    -   [SQLite3::loadExtension](sqlite3.loadextension.html) — Спробувати завантажити бібліотеку модуля SQLite
    -   [SQLite3::open](sqlite3.open.html) — Відкрити базу даних SQLite
    -   [SQLite3::openBlob](sqlite3.openblob.html) — Відкриває ресурс потоку для читання BLOB
    -   [SQLite3::prepare](sqlite3.prepare.html) — Підготовляє SQL-запит для виконання
    -   [SQLite3::query](sqlite3.query.html) - Виконує SQL-запит
    -   [SQLite3::querySingle](sqlite3.querysingle.html) — Виконує запит та повертає одиночний результат
    -   [SQLite3::setAuthorizer](sqlite3.setauthorizer.html) — Встановлює callback-функцію, яка використовуватиметься як авторизатор для обмеження дій висловлювання
    -   [SQLite3::version](sqlite3.version.html) — Повертає версію бібліотеки SQLite3, містить як рядкову константу, так і цифрову
-   [SQLite3Stmt](class.sqlite3stmt.html) - Клас SQLite3Stmt
    -   [SQLite3Stmt::bindParam](sqlite3stmt.bindparam.html) — Зв'язує параметр із змінною підготовленого запиту
    -   [SQLite3Stmt::bindValue](sqlite3stmt.bindvalue.html) — Зв'язує значення параметра зі змінною підготовленого запиту
    -   [SQLite3Stmt::clear](sqlite3stmt.clear.html) — Видаляє всі поточні параметри.
    -   [SQLite3Stmt::close](sqlite3stmt.close.html) - Закриває підготовлений запит
    -   [SQLite3Stmt::construct](sqlite3stmt.construct.html) - Конструктор класу SQLite3Stmt
    -   [SQLite3Stmt::execute](sqlite3stmt.execute.html) — Виконує підготовлений запит та повертає об'єкт із результуючим набором
    -   [SQLite3Stmt::getSQL](sqlite3stmt.getsql.html) — Отримати SQL-запит у вигляді рядка із запиту
    -   [SQLite3Stmt::paramCount](sqlite3stmt.paramcount.html) — Повертає кількість параметрів у підготовленому запиті
    -   [SQLite3Stmt::readOnly](sqlite3stmt.readonly.html) — Перевіряє, чи є підготовлений запит лише для читання
    -   [SQLite3Stmt::reset](sqlite3stmt.reset.html) - Скидає підготовлений запит
-   [SQLite3Result](class.sqlite3result.html) - Клас SQLite3Result
    -   [SQLite3Result::columnName](sqlite3result.columnname.html) — >Повертає ім'я n-ого стовпця
    -   [SQLite3Result::columnType](sqlite3result.columntype.html) - Повертає тип n-ного стовпця
    -   [SQLite3Result::construct](sqlite3result.construct.html) - Конструктор класу SQLite3Result
    -   [SQLite3Result::fetchArray](sqlite3result.fetcharray.html) — Вибирає один рядок з результуючого набору і поміщає його в асоціативний або нумерований масив, або в обох відразу
    -   [SQLite3Result::finalize](sqlite3result.finalize.html) - Закриває результуючий набір
    -   [SQLite3Result::numColumns](sqlite3result.numcolumns.html) — Повертає кількість стовпців у результуючому наборі
    -   [SQLite3Result::reset](sqlite3result.reset.html) — Скидає покажчик результуючого набору на перший рядок