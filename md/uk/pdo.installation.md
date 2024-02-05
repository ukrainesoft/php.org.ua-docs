---
navigation:
  - pdo.requirements.md: « Вимоги
  - pdo.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - pdo.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

**Встановлення PDO на Unix-системах**

1.  PDO та драйвер[PDO\_SQLITE](ref.pdo-sqlite.md)включені за замовчуванням у PHP. Щоб увімкнути PDO драйвер для довільної бази даних, зверніться до документації[драйвери PDO баз даних](pdo.drivers.md)
    
    > **Зауваження** :
    > 
    > Якщо PDO збирається, як модуль, що підвантажується (*не рекомендується*), то всі PDO-драйвери*повинні*бути завантажені*після*завантаження самого PDO.
    
2.  При встановленні PDO як модуля, що підвантажується, у файл php.ini необхідно внести зміни, щоб модуль PDO завантажувався автоматично при запуску PHP. Також туди доведеться увімкнути завантаження деяких драйверів баз даних; переконайтеся, що вони перераховані після рядка pdo.so, оскільки PDO повинен завантажитися першим. Якщо ви встановлюєте PDO та драйвери баз даних як статичні модулі, цей крок можна пропустити.
    
    ```
    extension=pdo.so
    ```
    

**Користувачі Windows**

1.  Виберіть DLL конкретних баз даних або завантажувати їх під час виконання функцією[dl()](function.dl.md), або включити їх у php.ini після php\_pdo.dll. Наприклад:
    
    ```
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
    ```
    
    Ці DLL повинні бути в директорії[extension\_dir](ini.core.md#ini.extension-dir)
    

> **Зауваження** :
> 
> Не забувайте, що після внесення змін до php.ini необхідний перезапуск PHP, щоб нові опції конфігурації набули чинності.
