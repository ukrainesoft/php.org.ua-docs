---
navigation:
  - install.pecl.intro.md: « Введення в установку PECL
  - install.pecl.windows.md: Встановлення PHP-модуля у Windows »
  - index.md: PHP Manual
  - install.pecl.md: Встановлення модулів PECL
title: Завантаження модулів PECL
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Завантаження модулів PECL

Є кілька варіантів для завантаження модулів PECL, зокрема:

-   Команда**pecl install extname**автоматично завантажує код модуля, тому в цьому випадку немає потреби окремого завантаження цих файлів.
    
-   [» https://pecl.php.net/](https://pecl.php.net/)Веб-сайт PECL містить інформацію про різні модулі, що надаються командою розробників PHP. Доступна на цьому веб-сайті інформація включає лог змін, новини релізів, вимоги та інші подібні деталі.
    
-   **pecl download extname**Модулі PECL, випуски яких перераховані на сайті PECL, доступні для скачування та встановлення за допомогою[» команди pecl](https://pear.php.net/manual/en/guide.users.commandline.cli.php). Також можна вказати окремі ревізії для встановлення.
    
-   git Багато модулів PECL знаходяться на GitHub.
    
-   SVN Деякі модулі PECL також знаходяться у SVN. Веб-інтерфейс для перегляду доступний за адресою[» https://svn.php.net/pecl/](https://svn.php.net/pecl/). Для завантаження безпосередньо з SVN можна виконати таку послідовність команд:
    
    $ svn checkout[https://svn.php.net/repository/pecl/extname/trunk](https://svn.php.net/repository/pecl/extname/trunk)extname
    
-   Завантаження для Windows Проект PHP компілює та пропонує файли DLL для Windows для більшості модулів PECL на сторінці з пакетами.
