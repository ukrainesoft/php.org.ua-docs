- [« Вимоги](pdo.requirements.md)
- [Налаштування під час виконання »](pdo.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](pdo.setup.md)
- Встановлення

## Установка

**Установка PDO на Unix-системах**

1. PDO та драйвер [PDO_SQLITE](ref.pdo-sqlite.md) включені по
замовчуванням у PHP. Щоб увімкнути PDO драйвер для довільної бази
даних, зверніться до документації [драйвери PDO баз даних](pdo.drivers.md).

> **Примітка**:
>
> Якщо PDO збирається, як модуль, що підвантажується (*не рекомендується*),
> то всі PDO-драйвери *мають* бути завантажені *після* завантаження
> PDO.

2. При установці PDO як підвантажуваний модуль у файл php.ini
необхідно внести зміни, щоб PDO завантажувався
автоматично під час запуску PHP. Також туди доведеться включити завантаження
деяких драйверів бази даних; при цьому переконайтесь, що вони
перераховані після рядка pdo.so, тому що PDO повинен завантажитися
першим. Якщо ви встановлюєте PDO та драйвери баз даних як
статичні модулі, цей крок можна пропустити.

extension=pdo.so

**Користувачі Windows**

1. Виберіть DLL конкретних баз даних або завантажити їх під час
виконання функцією [dl()](function.dl.md), або включити їх у
`php.ini` після `php_pdo.dll`. Наприклад:

extension=php_pdo.dll
extension=php_pdo_firebird.dll
extension=php_pdo_informix.dll
extension=php_pdo_mssql.dll
extension=php_pdo_mysql.dll
extension=php_pdo_oci.dll
extension=php_pdo_oci8.dll
extension=php_pdo_odbc.dll
extension=php_pdo_pgsql.dll
extension=php_pdo_sqlite.dll

Ці DLL повинні бути в директорії
[extension_dir](ini.core.md#ini.extension-dir).

> **Примітка**:
>
> Не забувайте, що після внесення змін до `php.ini` необхідний
> перезапуск PHP, щоб нові опції конфігурації набрали чинності.
