---
navigation:
  - mysql-xdevapi-schemaobject.getschema.md: '« SchemaObject::getSchema'
  - mysql-xdevapi-session.close.md: 'Session::close »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysqlxdevapi
title: Клас Session
---
# Клас Session

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\Session
     
     {


    /* Методы */
    
   public close(): bool
public commit(): Object
public createSchema(string $schema_name): mysql_xdevapi\Schema
public dropSchema(string $schema_name): bool
public generateUUID(): string
public getDefaultSchema(): string
public getSchema(string $schema_name): mysql_xdevapi\Schema
public getSchemas(): array
public getServerVersion(): int
public listClients(): array
public quoteName(string $name): string
public releaseSavepoint(string $name): void
public rollback(): void
public rollbackTo(string $name): void
public setSavepoint(string $name = ?): string
public sql(string $query): mysql_xdevapi\SqlStatement
public startTransaction(): void

   }
```

## Зміст

-   [Session::close](mysql-xdevapi-session.close.md) - Закриває сесію
-   [Session::commit](mysql-xdevapi-session.commit.md) - Фіксує транзакцію
-   [Session::construct](mysql-xdevapi-session.construct.md) - Опис конструктора
-   [Session::createSchema](mysql-xdevapi-session.createschema.md) - Створює нову схему
-   [Session::dropSchema](mysql-xdevapi-session.dropschema.md) - Видаляє схему
-   [Session::generateUUID](mysql-xdevapi-session.generateuuid.md) — Отримує новий UUID
-   [Session::getDefaultSchema](mysql-xdevapi-session.getdefaultschema.md) — Отримує ім'я схеми за умовчанням
-   [Session::getSchema](mysql-xdevapi-session.getschema.md) — Отримує новий об'єкт схеми
-   [Session::getSchemas](mysql-xdevapi-session.getschemas.md) — Отримує схеми
-   [Session::getServerVersion](mysql-xdevapi-session.getserverversion.md) — Отримує версію сервера
-   [Session::listClients](mysql-xdevapi-session.listclients.md) — Отримує список клієнтів
-   [Session::quoteName](mysql-xdevapi-session.quotename.md) - Додає лапки
-   [Session::releaseSavepoint](mysql-xdevapi-session.releasesavepoint.md) — Скасує встановлену точку збереження
-   [Session::rollback](mysql-xdevapi-session.rollback.md) - Відкочує транзакцію
-   [Session::rollbackTo](mysql-xdevapi-session.rollbackto.md) - Відкочує транзакцію до точки збереження
-   [Session::setSavepoint](mysql-xdevapi-session.setsavepoint.md) — Створює точку збереження
-   [Session::sql](mysql-xdevapi-session.sql.md) - Виконує SQL запит
-   [Session::startTransaction](mysql-xdevapi-session.starttransaction.md) - Починає транзакцію
