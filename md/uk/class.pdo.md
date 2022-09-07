---
navigation:
  - pdo.lobs.md: « Великі об'єкти (LOB)
  - pdo.begintransaction.md: 'PDO::beginTransaction »'
  - index.md: PHP Manual
  - book.pdo.md: PDO
title: Клас PDO
---
# Клас PDO

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.1.0)

## Вступ

З'єднання між PHP і сервером бази даних.

## Огляд класів

```classsynopsis

     
    

    
     
      class PDO
     
     {

    /* Методы */
    
   public __construct(    string $dsn,    ?string $username = null,    ?string $password = null,    ?array $options = null)

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
public query(    string $query,    ?int $fetchMode = PDO::FETCH_CLASS,    string $classname,    array $constructorArgs): PDOStatement|false
public query(string $query, ?int $fetchMode = PDO::FETCH_INTO, object $object): PDOStatement|false
public quote(string $string, int $type = PDO::PARAM_STR): string|false
public rollBack(): bool
public setAttribute(int $attribute, mixed $value): bool

   }
```

## Зміст

-   [PDO::beginTransaction](pdo.begintransaction.md) - Ініціалізація транзакції
-   [PDO::commit](pdo.commit.md) - Фіксує транзакцію
-   [PDO::construct](pdo.construct.md) — Створює екземпляр PDO, що надає з'єднання з базою даних
-   [PDO::errorCode](pdo.errorcode.md) — Повертає код SQLSTATE результату останньої операції з базою даних
-   [PDO::errorInfo](pdo.errorinfo.md) — Отримує розширену інформацію про помилку, що сталася під час останнього звернення до бази даних
-   [PDO::exec](pdo.exec.md) — Виконує SQL-запит та повертає кількість порушених рядків
-   [PDO::getAttribute](pdo.getattribute.md) — Отримати атрибут з'єднання з базою даних
-   [PDO::getAvailableDrivers](pdo.getavailabledrivers.md) - Повертає масив доступних драйверів PDO
-   [PDO::inTransaction](pdo.intransaction.md) — Перевіряє, чи розпочато транзакцію
-   [PDO::lastInsertId](pdo.lastinsertid.md) — Повертає ID останнього вставленого рядка або значення послідовності
-   [PDO::prepare](pdo.prepare.md) — готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDO::query](pdo.query.md) — Підготовляє та виконує вираз SQL без наповнювачів
-   [PDO::quote](pdo.quote.md) — Укладає рядок у лапки для використання у запиті
-   [PDO::rollBack](pdo.rollback.md) - Відкат транзакції
-   [PDO::setAttribute](pdo.setattribute.md) - Встановлення атрибуту
