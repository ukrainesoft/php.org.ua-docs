Функції SQLite (PDOSQLITE)

-   [« PDO::pgsqlLOBUnlink](pdo.pgsqllobunlink.md)
    
-   [PDOSQLITE DSN »](ref.pdo-sqlite.connection.html)
    
-   [PHP Manual](index.md)
    
-   [Драйвери PDO](pdo.drivers.md)
    
-   Функції SQLite (PDOSQLITE)
    

# Функції SQLite (PDOSQLITE)

## Вступ

PDOSQLITE це драйвер, який реалізує [интерфейс Data Objects (PDO)](intro.pdo.md) для доступу до баз даних SQLite 3.

> **Зауваження**
> 
> PDOSQLITE дозволяє використовувати рядки крім потоків разом з **`PDO::PARAM_LOB`**

## Встановлення

Драйвер PDOSQLITE PDO доступний за замовчуванням. Для вимкнення використовуйте **\-without-pdo-sqlite=DIR**, де `[=DIR]` - Директорія, куди встановлений SQLite. Починаючи з PHP 7.4.0 потрібна бібліотека [» libsqlite](http://sqlite.org/) версії 3.5.0 чи новіші. Раніше вбудований з коробки libsqlite міг використовуватися натомість, і був значенням за замовчуванням, якщо опція `[=DIR]` не задано.

> **Зауваження** **Додаткове налаштування на Windows з PHP 7.4.0**
> 
> Для роботи цього модуля системної змінної Windows PATH повинні бути доступні DLLфайли. Щоб дізнатися, як цього досягти, зверніться до розділу FAQ "[Як додати мою директорію з PHP до змінної Windows PATH](faq.installation.html#faq.installation.addtopath)". Хоча копіювання DLL-файлів з директорії PHP до системної папки Windows також вирішує проблему (бо системна директорія за умовчанням знаходиться в змінній PATH), це не рекомендується . *Цей модуль потребує наступних файлів у змінній PATH:* libsqlite3.dll.

## Зміст

-   [PDOSQLITE DSN](ref.pdo-sqlite.connection.html) — З'єднання з базою даних SQLite
-   [PDO::sqliteCreateAggregate](pdo.sqlitecreateaggregate.md) — Реєстрація агрегуючої функції користувача для використання в SQL-запитах
-   [PDO::sqliteCreateCollation](pdo.sqlitecreatecollation.md) — Реєстрація функції сортування для використання в SQL-запитах
-   [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md) — Реєстрація функції користувача для використання в SQL-запитах