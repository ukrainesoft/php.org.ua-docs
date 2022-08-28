Клас SQLite3

-   [« Предопределённые константы](sqlite3.constants.html)
    
-   [SQLite3::backup »](sqlite3.backup.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3](book.sqlite3.html)
    
-   Клас SQLite3
    

# Клас SQLite3

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас, що надає доступ до API SQLite 3 бази даних.

## Огляд класів

```classsynopsis

     
    

    
     
      class SQLite3
     
     {

    /* Методы */
    
   public __construct(string $filename, int $flags = SQLITE3_OPEN_READWRITE | SQLITE3_OPEN_CREATE, string $encryptionKey = "")

    public backup(SQLite3 $destination, string $sourceDatabase = "main", string $destinationDatabase = "main"): bool
public busyTimeout(int $milliseconds): bool
public changes(): int
public close(): bool
public createAggregate(    string $name,    callable $stepCallback,    callable $finalCallback,    int $argCount = -1): bool
public createCollation(string $name, callable $callback): bool
public createFunction(    string $name,    callable $callback,    int $argCount = -1,    int $flags = 0): bool
public enableExceptions(bool $enable = false): bool
public static escapeString(string $string): string
public exec(string $query): bool
public lastErrorCode(): int
public lastErrorMsg(): string
public lastInsertRowID(): int
public loadExtension(string $name): bool
public open(string $filename, int $flags = SQLITE3_OPEN_READWRITE | SQLITE3_OPEN_CREATE, string $encryptionKey = ""): void
public openBlob(    string $table,    string $column,    int $rowid,    string $database = "main",    int $flags = SQLITE3_OPEN_READONLY): resource|false
public prepare(string $query): SQLite3Stmt|false
public query(string $query): SQLite3Result|false
public querySingle(string $query, bool $entireRow = false): mixed
public setAuthorizer(?callable $callback): bool
public static version(): array

   }
```

## Зміст

-   [SQLite3::backup](sqlite3.backup.html) — Резервне копіювання однієї бази даних до іншої
-   [SQLite3::busyTimeout](sqlite3.busytimeout.html) - Встановити обробник "зайнято" на з'єднання
-   [SQLite3::changes](sqlite3.changes.html) — Отримати кількість рядків, які були змінені/віддалені/вставлені останнім запитом
-   [SQLite3::close](sqlite3.close.html) — Закрити з'єднання з базою даних
-   [SQLite3::\_\_construct](sqlite3.construct.html) — Створює екземпляр SQLite3 і відкриває з'єднання з базою
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