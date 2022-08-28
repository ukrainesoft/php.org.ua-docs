Встановлення

-   [« Требования](pgsql.requirements.html)
    
-   [Настройка во время выполнения »](pgsql.configuration.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](pgsql.setup.html)
    
-   Встановлення
    

## Встановлення

Для того, щоб увімкнути підтримку PostgreSQL, необхідно скомпілювати PHP з директивою **\-with-pgsql=DIR**. Параметр `DIR` визначає шлях до настановної директорії PostgreSQL, за умовчанням це /usr/local/pgsql. Якщо доступний динамічний модуль, він може бути включений директивою [extension](ini.core.html#ini.extension) у php.ini, або функцією [dl()](function.dl.html)