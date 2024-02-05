---
navigation:
  - pdo.pgsqllobunlink.md: '« PDO::pgsqlLOBUnlink'
  - ref.pdo-sqlite.connection.md: PDO\_SQLITE DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції SQLite (PDO\_SQLITE)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції SQLite (PDO\_SQLITE)

## Вступ

PDO\_SQLITE це драйвер, який реалізує [інтерфейс Data Objects (PDO)](intro.pdo.md) для доступу до баз даних SQLite 3.

> **Зауваження** :
> 
> PDO\_SQLITE дозволяє використовувати рядки крім потоків разом з **`PDO::PARAM_LOB`**

## Установка

Драйвер PDO\_SQLITE PDO доступен по умолчанию. Для отключения используйте**\--without-pdo-sqlite\[=DIR\]**, где`[=DIR]`\- директория, куда установлен sqlite. Начиная с PHP 7.4.0 требуется библиотека[» libsqlite](http://sqlite.org/) версії 3.5.0 чи новіші. Раніше вбудований з коробки libsqlite міг використовуватися натомість, і був значенням за замовчуванням, якщо опція `[=DIR]`не задана.

> **Зауваження** **Додаткове налаштування на Windows з PHP 7.4.0**
> 
> Для роботи цього модуля системної змінної Windows PATH повинні бути доступні DLL-файли. Щоб дізнатися, як цього досягти, зверніться до розділу FAQ "[Як додати мою директорію з PHP до змінної Windows PATH](faq.installation.md#faq.installation.addtopath)". Хоча копіювання DLL-файлів з директорії PHP до системної папки Windows також вирішує проблему (бо системна директорія за умовчанням знаходиться в змінній PATH), це не рекомендується. . \*Цей модуль потребує наступних файлів у змінній PATH:\*libsqlite3.dll.

## Зміст

-   [PDO\_SQLITE DSN](ref.pdo-sqlite.connection.md)— З'єднання з базою даних SQLite
-   [PDO::sqliteCreateAggregate](pdo.sqlitecreateaggregate.md)— Реєстрація агрегуючої функції користувача для використання в SQL-запитах
-   [PDO::sqliteCreateCollation](pdo.sqlitecreatecollation.md)— Реєстрація функції сортування для використання в SQL-запитах
-   [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md)— Реєстрація функції користувача для використання в SQL-запитах
