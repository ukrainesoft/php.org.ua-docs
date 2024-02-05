---
navigation:
  - pdo.lobs.md: « Великі об'єкти (LOB)
  - pdo.begintransaction.md: 'PDO::beginTransaction »'
  - index.md: PHP Manual
  - book.pdo.md: PDO
title: Клас PDO
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас PDO

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

## Вступ

З'єднання між PHP і сервером бази даних.

## Огляд класів

```classsynopsis

    
     class PDO
     {

    /* Константы */
    
     public
     const
     int
      PARAM_NULL;

    public
     const
     int
      PARAM_BOOL = 5;

    public
     const
     int
      PARAM_INT = 1;

    public
     const
     int
      PARAM_STR = 2;

    public
     const
     int
      PARAM_LOB = 3;

    public
     const
     int
      PARAM_STMT = 4;

    public
     const
     int
      PARAM_INPUT_OUTPUT;

    public
     const
     int
      PARAM_STR_NATL;

    public
     const
     int
      PARAM_STR_CHAR;

    public
     const
     int
      PARAM_EVT_ALLOC;

    public
     const
     int
      PARAM_EVT_FREE;

    public
     const
     int
      PARAM_EVT_EXEC_PRE;

    public
     const
     int
      PARAM_EVT_EXEC_POST;

    public
     const
     int
      PARAM_EVT_FETCH_PRE;

    public
     const
     int
      PARAM_EVT_FETCH_POST;

    public
     const
     int
      PARAM_EVT_NORMALIZE;

    public
     const
     int
      FETCH_DEFAULT;

    public
     const
     int
      FETCH_LAZY;

    public
     const
     int
      FETCH_ASSOC;

    public
     const
     int
      FETCH_NUM;

    public
     const
     int
      FETCH_BOTH;

    public
     const
     int
      FETCH_OBJ;

    public
     const
     int
      FETCH_BOUND;

    public
     const
     int
      FETCH_COLUMN;

    public
     const
     int
      FETCH_CLASS;

    public
     const
     int
      FETCH_INTO;

    public
     const
     int
      FETCH_FUNC;

    public
     const
     int
      FETCH_GROUP;

    public
     const
     int
      FETCH_UNIQUE;

    public
     const
     int
      FETCH_KEY_PAIR;

    public
     const
     int
      FETCH_CLASSTYPE;

    public
     const
     int
      FETCH_SERIALIZE;

    public
     const
     int
      FETCH_PROPS_LATE;

    public
     const
     int
      FETCH_NAMED;

    public
     const
     int
      ATTR_AUTOCOMMIT;

    public
     const
     int
      ATTR_PREFETCH;

    public
     const
     int
      ATTR_TIMEOUT;

    public
     const
     int
      ATTR_ERRMODE;

    public
     const
     int
      ATTR_SERVER_VERSION;

    public
     const
     int
      ATTR_CLIENT_VERSION;

    public
     const
     int
      ATTR_SERVER_INFO;

    public
     const
     int
      ATTR_CONNECTION_STATUS;

    public
     const
     int
      ATTR_CASE;

    public
     const
     int
      ATTR_CURSOR_NAME;

    public
     const
     int
      ATTR_CURSOR;

    public
     const
     int
      ATTR_ORACLE_NULLS;

    public
     const
     int
      ATTR_PERSISTENT;

    public
     const
     int
      ATTR_STATEMENT_CLASS;

    public
     const
     int
      ATTR_FETCH_TABLE_NAMES;

    public
     const
     int
      ATTR_FETCH_CATALOG_NAMES;

    public
     const
     int
      ATTR_DRIVER_NAME;

    public
     const
     int
      ATTR_STRINGIFY_FETCHES;

    public
     const
     int
      ATTR_MAX_COLUMN_LEN;

    public
     const
     int
      ATTR_EMULATE_PREPARES;

    public
     const
     int
      ATTR_DEFAULT_FETCH_MODE;

    public
     const
     int
      ATTR_DEFAULT_STR_PARAM;

    public
     const
     int
      ERRMODE_SILENT;

    public
     const
     int
      ERRMODE_WARNING;

    public
     const
     int
      ERRMODE_EXCEPTION;

    public
     const
     int
      CASE_NATURAL;

    public
     const
     int
      CASE_LOWER;

    public
     const
     int
      CASE_UPPER;

    public
     const
     int
      NULL_NATURAL;

    public
     const
     int
      NULL_EMPTY_STRING;

    public
     const
     int
      NULL_TO_STRING;

    public
     const
     string
      ERR_NONE;

    public
     const
     int
      FETCH_ORI_NEXT;

    public
     const
     int
      FETCH_ORI_PRIOR;

    public
     const
     int
      FETCH_ORI_FIRST;

    public
     const
     int
      FETCH_ORI_LAST;

    public
     const
     int
      FETCH_ORI_ABS;

    public
     const
     int
      FETCH_ORI_REL;

    public
     const
     int
      CURSOR_FWDONLY;

    public
     const
     int
      CURSOR_SCROLL;


    /* Методы */
    
   public __construct(    string $dsn,    ?string $username = null,    ?string $password = null,    ?array $options = null)

    public beginTransaction(): bool
public commit(): bool
public errorCode(): ?string
public errorInfo(): array
public exec(string $statement): int|false
public getAttribute(int $attribute): mixed
public static getAvailableDrivers(): array
public inTransaction(): bool
public lastInsertId(?string $name = null): string|false
public prepare(string $query, array $options = []): PDOStatement|false
public query(string $query, ?int $fetchMode = null): PDOStatement|false
public query(string $query, ?int $fetchMode = PDO::FETCH_COLUMN, int $colno): PDOStatement|false
public query(    string $query,    ?int $fetchMode = PDO::FETCH_CLASS,    string $classname,    array $constructorArgs): PDOStatement|false
public query(string $query, ?int $fetchMode = PDO::FETCH_INTO, object $object): PDOStatement|false
public quote(string $string, int $type = PDO::PARAM_STR): string|false
public rollBack(): bool
public setAttribute(int $attribute, mixed $value): bool

   }
```

## Зміст

-   [PDO::beginTransaction](pdo.begintransaction.md) \- Ініціалізація транзакції
-   [PDO::commit](pdo.commit.md) \- Фіксує транзакцію
-   [PDO::\_\_construct](pdo.construct.md)— Створює екземпляр PDO, що надає з'єднання з базою даних
-   [PDO::errorCode](pdo.errorcode.md)— Повертає код SQLSTATE результату останньої операції з базою даних
-   [PDO::errorInfo](pdo.errorinfo.md)— Отримує розширену інформацію про помилку, що сталася під час останнього звернення до бази даних
-   [PDO::exec](pdo.exec.md)— Виконує SQL-запит та повертає кількість порушених рядків
-   [PDO::getAttribute](pdo.getattribute.md)— Отримує атрибут з'єднання з базою даних
-   [PDO::getAvailableDrivers](pdo.getavailabledrivers.md) \- Повертає масив доступних драйверів PDO
-   [PDO::inTransaction](pdo.intransaction.md)— Перевіряє, чи розпочато транзакцію
-   [PDO::lastInsertId](pdo.lastinsertid.md)— Повертає ID останнього вставленого рядка або значення послідовності
-   [PDO::prepare](pdo.prepare.md)— готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDO::query](pdo.query.md)— Готує та виконує вираз SQL без наповнювачів
-   [PDO::quote](pdo.quote.md)— Укладає рядок у лапки для використання у запиті
-   [PDO::rollBack](pdo.rollback.md) \- Відкат транзакції
-   [PDO::setAttribute](pdo.setattribute.md) \- Встановлення атрибуту
