---
navigation:
  - mysql-xdevapi-schemaobject.getschema.html: '« SchemaObject::getSchema'
  - mysql-xdevapi-session.close.html: 'Session::close »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
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

-   [Session::close](mysql-xdevapi-session.close.html) - Закриває сесію
-   [Session::commit](mysql-xdevapi-session.commit.html) - Фіксує транзакцію
-   [Session::construct](mysql-xdevapi-session.construct.html) - Опис конструктора
-   [Session::createSchema](mysql-xdevapi-session.createschema.html) - Створює нову схему
-   [Session::dropSchema](mysql-xdevapi-session.dropschema.html) - Видаляє схему
-   [Session::generateUUID](mysql-xdevapi-session.generateuuid.html) — Отримує новий UUID
-   [Session::getDefaultSchema](mysql-xdevapi-session.getdefaultschema.html) — Отримує ім'я схеми за умовчанням
-   [Session::getSchema](mysql-xdevapi-session.getschema.html) — Отримує новий об'єкт схеми
-   [Session::getSchemas](mysql-xdevapi-session.getschemas.html) — Отримує схеми
-   [Session::getServerVersion](mysql-xdevapi-session.getserverversion.html) — Отримує версію сервера
-   [Session::listClients](mysql-xdevapi-session.listclients.html) — Отримує список клієнтів
-   [Session::quoteName](mysql-xdevapi-session.quotename.html) - Додає лапки
-   [Session::releaseSavepoint](mysql-xdevapi-session.releasesavepoint.html) — Скасує встановлену точку збереження
-   [Session::rollback](mysql-xdevapi-session.rollback.html) - Відкочує транзакцію
-   [Session::rollbackTo](mysql-xdevapi-session.rollbackto.html) - Відкочує транзакцію до точки збереження
-   [Session::setSavepoint](mysql-xdevapi-session.setsavepoint.html) — Створює точку збереження
-   [Session::sql](mysql-xdevapi-session.sql.html) - Виконує SQL запит
-   [Session::startTransaction](mysql-xdevapi-session.starttransaction.html) - Починає транзакцію
