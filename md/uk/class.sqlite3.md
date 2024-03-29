---
navigation:
  - sqlite3.constants.md: « Зумовлені константи
  - sqlite3.backup.md: 'SQLite3::backup »'
  - index.md: PHP Manual
  - book.sqlite3.md: SQLite3
title: Клас SQLite3
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SQLite3

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас, що надає доступ до API SQLite 3 бази даних.

## Огляд класів

```classsynopsis

    
     class SQLite3
     {

    /* Константы */
    
     public
     const
     int
      OK;

    public
     const
     int
      DENY;

    public
     const
     int
      IGNORE;

    public
     const
     int
      CREATE_INDEX;

    public
     const
     int
      CREATE_TABLE;

    public
     const
     int
      CREATE_TEMP_INDEX;

    public
     const
     int
      CREATE_TEMP_TABLE;

    public
     const
     int
      CREATE_TEMP_TRIGGER;

    public
     const
     int
      CREATE_TEMP_VIEW;

    public
     const
     int
      CREATE_TRIGGER;

    public
     const
     int
      CREATE_VIEW;

    public
     const
     int
      DELETE;

    public
     const
     int
      DROP_INDEX;

    public
     const
     int
      DROP_TABLE;

    public
     const
     int
      DROP_TEMP_INDEX;

    public
     const
     int
      DROP_TEMP_TABLE;

    public
     const
     int
      DROP_TEMP_TRIGGER;

    public
     const
     int
      DROP_TEMP_VIEW;

    public
     const
     int
      DROP_TRIGGER;

    public
     const
     int
      DROP_VIEW;

    public
     const
     int
      INSERT;

    public
     const
     int
      PRAGMA;

    public
     const
     int
      READ;

    public
     const
     int
      SELECT;

    public
     const
     int
      TRANSACTION;

    public
     const
     int
      UPDATE;

    public
     const
     int
      ATTACH;

    public
     const
     int
      DETACH;

    public
     const
     int
      ALTER_TABLE;

    public
     const
     int
      REINDEX;

    public
     const
     int
      ANALYZE;

    public
     const
     int
      CREATE_VTABLE;

    public
     const
     int
      DROP_VTABLE;

    public
     const
     int
      FUNCTION;

    public
     const
     int
      SAVEPOINT;

    public
     const
     int
      COPY;

    public
     const
     int
      RECURSIVE;


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

## Обумовлені константи

**`SQLite3::OK`**

**`SQLite3::DENY`**

**`SQLite3::IGNORE`**

**`SQLite3::CREATE_INDEX`**

**`SQLite3::CREATE_TABLE`**

**`SQLite3::CREATE_TEMP_INDEX`**

**`SQLite3::CREATE_TEMP_TABLE`**

**`SQLite3::CREATE_TEMP_TRIGGER`**

**`SQLite3::CREATE_TEMP_VIEW`**

**`SQLite3::CREATE_TRIGGER`**

**`SQLite3::CREATE_VIEW`**

**`SQLite3::DELETE`**

**`SQLite3::DROP_INDEX`**

**`SQLite3::DROP_TABLE`**

**`SQLite3::DROP_TEMP_INDEX`**

**`SQLite3::DROP_TEMP_TABLE`**

**`SQLite3::DROP_TEMP_TRIGGER`**

**`SQLite3::DROP_TEMP_VIEW`**

**`SQLite3::DROP_TRIGGER`**

**`SQLite3::DROP_VIEW`**

**`SQLite3::INSERT`**

**`SQLite3::PRAGMA`**

**`SQLite3::READ`**

**`SQLite3::SELECT`**

**`SQLite3::TRANSACTION`**

**`SQLite3::UPDATE`**

**`SQLite3::ATTACH`**

**`SQLite3::DETACH`**

**`SQLite3::ALTER_TABLE`**

**`SQLite3::REINDEX`**

**`SQLite3::ANALYZE`**

**`SQLite3::CREATE_VTABLE`**

**`SQLite3::DROP_VTABLE`**

**`SQLite3::FUNCTION`**

**`SQLite3::SAVEPOINT`**

**`SQLite3::COPY`**

**`SQLite3::RECURSIVE`**

## Зміст

-   [SQLite3::backup](sqlite3.backup.md)— Резервне копіювання однієї бази даних до іншої
-   [SQLite3::busyTimeout](sqlite3.busytimeout.md) - Встановити обробник "зайнято" на з'єднання
-   [SQLite3::changes](sqlite3.changes.md)— Отримати кількість рядків, які були змінені/віддалені/вставлені останнім запитом
-   [SQLite3::close](sqlite3.close.md)— Закрити з'єднання з базою даних
-   [SQLite3::\_\_construct](sqlite3.construct.md)— Створює екземпляр SQLite3 і відкриває з'єднання з базою
-   [SQLite3::createAggregate](sqlite3.createaggregate.md)— Зареєструвати функцію PHP як агрегуючу функцію SQL
-   [SQLite3::createCollation](sqlite3.createcollation.md)— Реєструє функцію PHP для використання як функцію сортування SQL
-   [SQLite3::createFunction](sqlite3.createfunction.md)— Реєструє функцію PHP для використання як скалярну функцію SQL
-   [SQLite3::enableExceptions](sqlite3.enableexceptions.md) \- Включити викид винятків
-   [SQLite3::escapeString](sqlite3.escapestring.md)— Повертає правильно екранований рядок
-   [SQLite3::exec](sqlite3.exec.md)— Виконує запит без результату до поточної бази даних
-   [SQLite3::lastErrorCode](sqlite3.lasterrorcode.md)— Повертає числовий код результату останнього запиту SQLite.
-   [SQLite3::lastErrorMsg](sqlite3.lasterrormsg.md)— Повертає текст англійською, що описує останній невдалий запит SQLite
-   [SQLite3::lastInsertRowID](sqlite3.lastinsertrowid.md)— Повертає ідентифікатор рядка останньої вставки (INSERT) до бази даних
-   [SQLite3::loadExtension](sqlite3.loadextension.md)— Спробувати завантажити бібліотеку модуля SQLite
-   [SQLite3::open](sqlite3.open.md)— Відкрити базу даних SQLite
-   [SQLite3::openBlob](sqlite3.openblob.md)— Відкриває ресурс потоку для читання BLOB
-   [SQLite3::prepare](sqlite3.prepare.md)— Підготовляє SQL-запит для виконання
-   [SQLite3::query](sqlite3.query.md) \- Виконує SQL-запит
-   [SQLite3::querySingle](sqlite3.querysingle.md)— Виконує запит та повертає одиночний результат
-   [SQLite3::setAuthorizer](sqlite3.setauthorizer.md)— Встановлює callback-функцію, яка використовуватиметься як авторизатор для обмеження дій висловлювання
-   [SQLite3::version](sqlite3.version.md)— Повертає версію бібліотеки SQLite3, містить як рядкову константу, так і цифрову
